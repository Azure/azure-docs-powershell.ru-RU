---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228732"
---
# <span data-ttu-id="0a9a9-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a9a9-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="0a9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0a9a9-103">Возвращает запись в ACL файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0a9a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a9a9-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a9a9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="0a9a9-106">Cmdlet **Get-AzDataLakeStoreItemAclEntry** получает запись (ACE) в списке управления доступом (ACL) файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0a9a9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="0a9a9-108">Пример 1. Получить ACL для папки</span><span class="sxs-lookup"><span data-stu-id="0a9a9-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="0a9a9-109">Эта команда получает ACL для корневого каталога указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="0a9a9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a9a9-110">PARAMETERS</span></span>

### <span data-ttu-id="0a9a9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0a9a9-111">-Account</span></span>
<span data-ttu-id="0a9a9-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0a9a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a9a9-113">-DefaultProfile</span></span>
<span data-ttu-id="0a9a9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a9a9-115">-Path</span><span class="sxs-lookup"><span data-stu-id="0a9a9-115">-Path</span></span>
<span data-ttu-id="0a9a9-116">Путь к элементу, для которого этот cmdlet получает ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="0a9a9-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0a9a9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a9a9-117">CommonParameters</span></span>
<span data-ttu-id="0a9a9-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a9a9-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a9a9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a9a9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a9a9-120">INPUTS</span></span>

### <span data-ttu-id="0a9a9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0a9a9-121">System.String</span></span>

### <span data-ttu-id="0a9a9-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0a9a9-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="0a9a9-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a9a9-123">OUTPUTS</span></span>

### <span data-ttu-id="0a9a9-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="0a9a9-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="0a9a9-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a9a9-125">NOTES</span></span>

## <span data-ttu-id="0a9a9-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a9a9-126">RELATED LINKS</span></span>

[<span data-ttu-id="0a9a9-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a9a9-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="0a9a9-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a9a9-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


