---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400359"
---
# <span data-ttu-id="225a5-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="225a5-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="225a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="225a5-102">SYNOPSIS</span></span>
<span data-ttu-id="225a5-103">Получает разрешение восьмеричего разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="225a5-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="225a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="225a5-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="225a5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="225a5-105">DESCRIPTION</span></span>
<span data-ttu-id="225a5-106">Cmdlet **Get-AzDataLakeStoreItemPermission** получает восьмеричное разрешение файла или папки в хранилище Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="225a5-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="225a5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="225a5-107">EXAMPLES</span></span>

### <span data-ttu-id="225a5-108">Пример 1. Настройка восьмяльного разрешения для файла</span><span class="sxs-lookup"><span data-stu-id="225a5-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="225a5-109">Эта команда получает восьмяльное разрешение для файла.</span><span class="sxs-lookup"><span data-stu-id="225a5-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="225a5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="225a5-110">PARAMETERS</span></span>

### <span data-ttu-id="225a5-111">-Account</span><span class="sxs-lookup"><span data-stu-id="225a5-111">-Account</span></span>
<span data-ttu-id="225a5-112">Указывает имя учетной записи Для магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="225a5-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="225a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225a5-113">-DefaultProfile</span></span>
<span data-ttu-id="225a5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="225a5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="225a5-115">-Path</span><span class="sxs-lookup"><span data-stu-id="225a5-115">-Path</span></span>
<span data-ttu-id="225a5-116">Путь к файлу или папке из магазина данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="225a5-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="225a5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225a5-117">CommonParameters</span></span>
<span data-ttu-id="225a5-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225a5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225a5-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225a5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225a5-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="225a5-120">INPUTS</span></span>

### <span data-ttu-id="225a5-121">System.String</span><span class="sxs-lookup"><span data-stu-id="225a5-121">System.String</span></span>

### <span data-ttu-id="225a5-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="225a5-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="225a5-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="225a5-123">OUTPUTS</span></span>

### <span data-ttu-id="225a5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="225a5-124">System.String</span></span>

## <span data-ttu-id="225a5-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="225a5-125">NOTES</span></span>
* <span data-ttu-id="225a5-126">Псевдоним: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="225a5-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="225a5-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="225a5-127">RELATED LINKS</span></span>

[<span data-ttu-id="225a5-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="225a5-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


