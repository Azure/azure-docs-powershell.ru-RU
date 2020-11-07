---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733753"
---
# <span data-ttu-id="07661-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="07661-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="07661-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07661-102">SYNOPSIS</span></span>
<span data-ttu-id="07661-103">Возвращает запись в ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="07661-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07661-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07661-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07661-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07661-105">DESCRIPTION</span></span>
<span data-ttu-id="07661-106">Командлет **Get-AzureRmDataLakeStoreItemAclEntry** получает запись (ACE) в списке управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="07661-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="07661-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07661-107">EXAMPLES</span></span>

### <span data-ttu-id="07661-108">Пример 1: получение ACL для папки</span><span class="sxs-lookup"><span data-stu-id="07661-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="07661-109">Эта команда возвращает ACL для корневого каталога указанной учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="07661-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="07661-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07661-110">PARAMETERS</span></span>

### <span data-ttu-id="07661-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="07661-111">-Account</span></span>
<span data-ttu-id="07661-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="07661-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="07661-113">-Path</span><span class="sxs-lookup"><span data-stu-id="07661-113">-Path</span></span>
<span data-ttu-id="07661-114">Указывает путь к Data Lake Store для элемента, для которого этот командлет получает запись ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="07661-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="07661-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07661-115">-DefaultProfile</span></span>
<span data-ttu-id="07661-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07661-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07661-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07661-117">CommonParameters</span></span>
<span data-ttu-id="07661-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07661-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07661-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07661-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07661-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07661-120">INPUTS</span></span>

## <span data-ttu-id="07661-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07661-121">OUTPUTS</span></span>

### <span data-ttu-id="07661-122">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="07661-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="07661-123">Список записей ACL для указанной папки или файла.</span><span class="sxs-lookup"><span data-stu-id="07661-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="07661-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="07661-124">NOTES</span></span>

## <span data-ttu-id="07661-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07661-125">RELATED LINKS</span></span>

[<span data-ttu-id="07661-126">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="07661-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="07661-127">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="07661-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


