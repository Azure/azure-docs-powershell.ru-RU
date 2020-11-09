---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247184"
---
# <span data-ttu-id="adf80-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="adf80-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="adf80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="adf80-102">SYNOPSIS</span></span>
<span data-ttu-id="adf80-103">Создает объект фильтра правила ManagementPolicy, который можно использовать в New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="adf80-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="adf80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="adf80-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adf80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adf80-105">DESCRIPTION</span></span>
<span data-ttu-id="adf80-106">Командлет **New-AzStorageAccountManagementPolicyFilter** создает объект фильтра правила ManagementPolicy, который можно использовать в New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="adf80-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="adf80-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="adf80-107">EXAMPLES</span></span>

### <span data-ttu-id="adf80-108">Пример 1: создание объекта фильтра правила ManagementPolicy, затем добавление его в правило политики управления и назначение учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="adf80-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="adf80-109">Эта команда создает объект фильтра правила ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="adf80-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="adf80-110">Затем добавьте его в правило политики управления и установите для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="adf80-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="adf80-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="adf80-111">PARAMETERS</span></span>

### <span data-ttu-id="adf80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf80-112">-DefaultProfile</span></span>
<span data-ttu-id="adf80-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adf80-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adf80-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="adf80-114">-PrefixMatch</span></span>
<span data-ttu-id="adf80-115">Массив строк, для которых должны быть сопоставлены префиксы.</span><span class="sxs-lookup"><span data-stu-id="adf80-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="adf80-116">Строка префикса должна начинаться с имени контейнера.</span><span class="sxs-lookup"><span data-stu-id="adf80-116">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf80-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf80-117">CommonParameters</span></span>
<span data-ttu-id="adf80-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="adf80-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf80-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adf80-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf80-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="adf80-120">INPUTS</span></span>

### <span data-ttu-id="adf80-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="adf80-121">None</span></span>

## <span data-ttu-id="adf80-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="adf80-122">OUTPUTS</span></span>

### <span data-ttu-id="adf80-123">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="adf80-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="adf80-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="adf80-124">NOTES</span></span>

## <span data-ttu-id="adf80-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adf80-125">RELATED LINKS</span></span>