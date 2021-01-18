---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504587"
---
# <span data-ttu-id="7b051-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="7b051-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="7b051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b051-102">SYNOPSIS</span></span>
<span data-ttu-id="7b051-103">Получает разрешение восьмеричего разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7b051-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7b051-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b051-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b051-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b051-105">DESCRIPTION</span></span>
<span data-ttu-id="7b051-106">**Cmdlet Get-AzDataLakeStoreItemPermission** получает восьмеричное разрешение файла или папки в хранилище Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7b051-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7b051-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b051-107">EXAMPLES</span></span>

### <span data-ttu-id="7b051-108">Пример 1. Настройка восьмяльного разрешения для файла</span><span class="sxs-lookup"><span data-stu-id="7b051-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="7b051-109">Эта команда получает восьмяльное разрешение для файла.</span><span class="sxs-lookup"><span data-stu-id="7b051-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="7b051-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b051-110">PARAMETERS</span></span>

### <span data-ttu-id="7b051-111">-Account</span><span class="sxs-lookup"><span data-stu-id="7b051-111">-Account</span></span>
<span data-ttu-id="7b051-112">Указывает имя учетной записи Для магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7b051-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="7b051-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b051-113">-DefaultProfile</span></span>
<span data-ttu-id="7b051-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b051-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b051-115">-Path</span><span class="sxs-lookup"><span data-stu-id="7b051-115">-Path</span></span>
<span data-ttu-id="7b051-116">Путь к файлу или папке из магазина данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="7b051-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7b051-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b051-117">CommonParameters</span></span>
<span data-ttu-id="7b051-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b051-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b051-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b051-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b051-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b051-120">INPUTS</span></span>

### <span data-ttu-id="7b051-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7b051-121">System.String</span></span>

### <span data-ttu-id="7b051-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7b051-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="7b051-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b051-123">OUTPUTS</span></span>

### <span data-ttu-id="7b051-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7b051-124">System.String</span></span>

## <span data-ttu-id="7b051-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b051-125">NOTES</span></span>
* <span data-ttu-id="7b051-126">Псевдоним: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="7b051-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="7b051-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b051-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b051-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="7b051-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


