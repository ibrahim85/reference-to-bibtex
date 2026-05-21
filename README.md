# Reference to BibTeX Converter

A comprehensive web application that converts academic references from Word, Excel, or plain text format into BibTeX entries using CrossRef.org and Google Scholar APIs.

## ✨ Features

- **Multiple Input Formats**: Support for Word documents (.docx), Excel spreadsheets (.xlsx), and plain text
- **Dual Search APIs**: CrossRef.org and Google Scholar integration
- **Automatic Metadata Extraction**: Intelligently extracts author, title, year, journal, volume, pages, DOI
- **BibTeX Generation**: Automatically generates properly formatted BibTeX entries
- **Batch Processing**: Convert multiple references at once
- **Export Options**: Download as .bib file or copy individual entries
- **Web-based Interface**: No installation required, responsive design
- **Real-time Validation**: Verify references before conversion
- **Edit & Refine**: Manual editing capability for each entry



## 📖 API Documentation

### POST `/api/references/upload`
Upload file (docx, xlsx) or paste text
```json
{
  "type": "text",
  "content": "Abd El-Hack, M. E., El-Saadony, M. T., ..."
}
```

### POST `/api/references/parse`
Parse reference text into structured data
```json
{
  "reference": "Abd El-Hack, M. E., El-Saadony, M. T., Nader, M. M., Salem, H. M., El-Tahan, A. M., Soliman, S. M., & Khafaga, A. F. (2022). Effect of environmental factors on growth performance of Nile tilapia (Oreochromis niloticus). International journal of biometeorology, 66(11), 2183-2194."
}
```

### POST `/api/references/search-crossref`
Search CrossRef for complete bibliographic data
```json
{
  "title": "Effect of environmental factors on growth performance of Nile tilapia",
  "authors": "Abd El-Hack",
  "year": "2022"
}
```

### POST `/api/bibtex/generate`
Generate BibTeX entry from structured data
```json
{
  "type": "article",
  "authors": ["Abd El-Hack, Mohamed E.", "El-Saadony, Mohamed T."],
  "title": "Effect of environmental factors on growth performance of Nile tilapia (Oreochromis niloticus)",
  "journal": "International Journal of Biometeorology",
  "year": 2022,
  "volume": 66,
  "number": 11,
  "pages": "2183-2194",
  "doi": "10.1007/s00484-022-02347-6"
}
```

## 💡 Usage Examples

### Example 1: Word Document
1. Click "Upload File"
2. Select your .docx file containing references
3. Click "Parse References"
4. Review extracted references
5. Click "Convert to BibTeX"
6. Download or copy entries

### Example 2: Plain Text
1. Click "Paste Text"
2. Paste your reference:
   ```
   Abd El-Hack, M. E., El-Saadony, M. T., Nader, M. M., Salem, H. M., El-Tahan, A. M., Soliman, S. M., & Khafaga, A. F. (2022). Effect of environmental factors on growth performance of Nile tilapia (Oreochromis niloticus). International journal of biometeorology, 66(11), 2183-2194.
   ```
3. Click "Search CrossRef"
4. View generated BibTeX
5. Export as needed

## 📤 Output Format

The application generates properly formatted BibTeX entries:

```bibtex
@article{Abd_El_Hack_2022,
  title={Effect of environmental factors on growth performance of Nile tilapia (Oreochromis niloticus)},
  volume={66},
  ISSN={1432-1254},
  url={http://dx.doi.org/10.1007/s00484-022-02347-6},
  DOI={10.1007/s00484-022-02347-6},
  number={11},
  journal={International Journal of Biometeorology},
  publisher={Springer Science and Business Media LLC},
  author={Abd El-Hack, Mohamed E. and El-Saadony, Mohamed T. and Nader, Maha M. and Salem, Heba M. and El-Tahan, Amira M. and Soliman, Soliman M. and Khafaga, Asmaa F.},
  year={2022},
  month={Aug},
  pages={2183--2194}
}
```

## 🔮 Future Enhancements

- 📅 Semantic Scholar API integration
- 📅 ORCID API for author validation
- 📅 Duplicate reference detection
- 📅 Citation format conversion (APA ↔ MLA ↔ Chicago)
- 📅 Browser extension for direct reference capture
- 📅 Collaboration features with real-time sync
- 📅 Machine learning for improved parsing accuracy
- 📅 Support for additional file formats (PDF, TXT)


## 📝 License

MIT License - see [LICENSE](LICENSE) file for details

## 🙏 Acknowledgments

- CrossRef.org for their excellent API
- All contributors and users

---

**Made with ❤️ for the academic community**
