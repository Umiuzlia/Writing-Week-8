# **Context**
Context dirancang untuk sharing data secara global seperti tema, bahasa pada komponen react.
## Cara penggunaan Context
1. Buatlah folder di dalam src dengan nama AppContext.js
- Import React Library
import React from "react"
- Definisikan variable dengan assign value React.createContext()
export const AppContext = React.createContext()
2. pada folder App.js lakukanlah import file yang ingin ditambahkan. 

        import { AppContext } from "./context/AppContext";
        import Home from "./page/home/Home";
        import Gallery from "./page/gallery/Gallery";

        function App() {
            const [theme, setThem] = useState("dark")

            return (
                <>
                    <AppContext.Provider value={{lang: "id", theme: theme, }}>
                </>
            )
        }



# **Testing**
> React Testing adalah library DOM dengan menambahkan API untuk bekerja dengan komponen React. Secara garis besar testing terbagi menjadi 2 yaitu: Manual Testing dan Automated Testing. untuk cara pebintalan Testing 
        npm install --save-dev@testing-library/react
## Tujuan penggunaan Testing
1. Untuk mencegah regresi. Regresi adalah kemunculan kembali bug yang sebelumnya telah diperbaiki. Itu membuat fitur berhenti berfungsi sebagaimana dimaksud setelah peristiwa tertentu terjadi.
2. Untuk memastikan fungsionalitas komponen kompleks dan aplikasi modular.
3. Untuk kinerja efektif dari aplikasi perangkat lunak atau produk.
### Step dari sebuah Testing 
- Assert
- Arrange
- Act
