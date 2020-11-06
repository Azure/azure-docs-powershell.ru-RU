---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 1743ee6e4d0ce1276c69bec9e3669b5d04ee3858
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567652"
---
# <span data-ttu-id="34aea-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="34aea-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="34aea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34aea-102">SYNOPSIS</span></span>
<span data-ttu-id="34aea-103">Получает восьмеричные разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34aea-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34aea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34aea-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34aea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34aea-105">DESCRIPTION</span></span>
<span data-ttu-id="34aea-106">Командлет **Get-AzureRmDataLakeStoreItemPermission** получает восьмеричные разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34aea-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="34aea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34aea-107">EXAMPLES</span></span>

### <span data-ttu-id="34aea-108">Пример 1: Установка восьмеричного разрешения для файла</span><span class="sxs-lookup"><span data-stu-id="34aea-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="34aea-109">Эта команда получает восьмеричное разрешение для файла.</span><span class="sxs-lookup"><span data-stu-id="34aea-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="34aea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34aea-110">PARAMETERS</span></span>

### <span data-ttu-id="34aea-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="34aea-111">-Account</span></span>
<span data-ttu-id="34aea-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34aea-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34aea-113">-Path</span><span class="sxs-lookup"><span data-stu-id="34aea-113">-Path</span></span>
<span data-ttu-id="34aea-114">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="34aea-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34aea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34aea-115">-DefaultProfile</span></span>
<span data-ttu-id="34aea-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34aea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34aea-117">CommonParameters</span></span>
<span data-ttu-id="34aea-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34aea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34aea-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34aea-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34aea-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34aea-120">INPUTS</span></span>

## <span data-ttu-id="34aea-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34aea-121">OUTPUTS</span></span>

### <span data-ttu-id="34aea-122">подстрок</span><span class="sxs-lookup"><span data-stu-id="34aea-122">string</span></span>
<span data-ttu-id="34aea-123">Строковое представление восьмеричного владельца</span><span class="sxs-lookup"><span data-stu-id="34aea-123">The string representation of the ownership octal</span></span>

## <span data-ttu-id="34aea-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="34aea-124">NOTES</span></span>
* <span data-ttu-id="34aea-125">Alias (псевдоним): Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="34aea-125">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="34aea-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34aea-126">RELATED LINKS</span></span>

[<span data-ttu-id="34aea-127">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="34aea-127">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


