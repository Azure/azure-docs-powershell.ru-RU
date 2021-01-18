---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507059"
---
# <span data-ttu-id="1af39-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="1af39-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="1af39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af39-102">SYNOPSIS</span></span>
<span data-ttu-id="1af39-103">Создание объекта фильтра правила ManagementPolicy, который можно использовать в new-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="1af39-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="1af39-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1af39-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1af39-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af39-105">DESCRIPTION</span></span>
<span data-ttu-id="1af39-106">Cmdlet **New-AzStorageAccountManagementPolicyFilter** создает объект фильтра правил ManagementPolicy, который можно использовать в new-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="1af39-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="1af39-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1af39-107">EXAMPLES</span></span>

### <span data-ttu-id="1af39-108">Пример 1. Создание объекта фильтра правил ManagementPolicy, его добавление в правило политики управления и настройка учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1af39-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="1af39-109">Эта команда создает объект фильтра правил ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="1af39-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="1af39-110">Затем добавьте его в правило политики управления и установите учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="1af39-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="1af39-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1af39-111">PARAMETERS</span></span>

### <span data-ttu-id="1af39-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af39-112">-DefaultProfile</span></span>
<span data-ttu-id="1af39-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1af39-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af39-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="1af39-114">-PrefixMatch</span></span>
<span data-ttu-id="1af39-115">Массив строк для совпадения префиксов.</span><span class="sxs-lookup"><span data-stu-id="1af39-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="1af39-116">Строка префикса должна начинаться с имени контейнера.</span><span class="sxs-lookup"><span data-stu-id="1af39-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="1af39-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af39-117">CommonParameters</span></span>
<span data-ttu-id="1af39-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af39-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af39-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af39-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af39-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1af39-120">INPUTS</span></span>

### <span data-ttu-id="1af39-121">Нет</span><span class="sxs-lookup"><span data-stu-id="1af39-121">None</span></span>

## <span data-ttu-id="1af39-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1af39-122">OUTPUTS</span></span>

### <span data-ttu-id="1af39-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="1af39-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="1af39-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1af39-124">NOTES</span></span>

## <span data-ttu-id="1af39-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1af39-125">RELATED LINKS</span></span>
