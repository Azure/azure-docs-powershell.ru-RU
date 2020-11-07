---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 3279ebd2b505a2d6563cdcabd497f83637c9c42c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731071"
---
# <span data-ttu-id="5d901-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5d901-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="5d901-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d901-102">SYNOPSIS</span></span>
<span data-ttu-id="5d901-103">Возвращает запись в ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d901-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5d901-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d901-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d901-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d901-105">DESCRIPTION</span></span>
<span data-ttu-id="5d901-106">Командлет **Get-AzDataLakeStoreItemAclEntry** получает запись (ACE) в списке управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d901-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5d901-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d901-107">EXAMPLES</span></span>

### <span data-ttu-id="5d901-108">Пример 1: получение ACL для папки</span><span class="sxs-lookup"><span data-stu-id="5d901-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="5d901-109">Эта команда возвращает ACL для корневого каталога указанной учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="5d901-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="5d901-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d901-110">PARAMETERS</span></span>

### <span data-ttu-id="5d901-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5d901-111">-Account</span></span>
<span data-ttu-id="5d901-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d901-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5d901-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d901-113">-DefaultProfile</span></span>
<span data-ttu-id="5d901-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d901-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d901-115">-Path</span><span class="sxs-lookup"><span data-stu-id="5d901-115">-Path</span></span>
<span data-ttu-id="5d901-116">Указывает путь к Data Lake Store для элемента, для которого этот командлет получает запись ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="5d901-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5d901-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d901-117">CommonParameters</span></span>
<span data-ttu-id="5d901-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d901-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d901-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d901-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d901-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d901-120">INPUTS</span></span>

### <span data-ttu-id="5d901-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5d901-121">System.String</span></span>

### <span data-ttu-id="5d901-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5d901-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="5d901-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d901-123">OUTPUTS</span></span>

### <span data-ttu-id="5d901-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="5d901-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="5d901-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d901-125">NOTES</span></span>

## <span data-ttu-id="5d901-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d901-126">RELATED LINKS</span></span>

[<span data-ttu-id="5d901-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5d901-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="5d901-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5d901-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


