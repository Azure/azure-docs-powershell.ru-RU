---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 40a2420803197b21bb9f0f8d20b771482b4e694b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002632"
---
# <span data-ttu-id="fe318-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="fe318-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="fe318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe318-102">SYNOPSIS</span></span>
<span data-ttu-id="fe318-103">Создание объекта фильтра правила ManagementPolicy, который можно использовать в new-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="fe318-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="fe318-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe318-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-BlobType <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe318-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe318-105">DESCRIPTION</span></span>
<span data-ttu-id="fe318-106">Cmdlet **New-AzStorageAccountManagementPolicyFilter** создает объект фильтра правил ManagementPolicy, который можно использовать в new-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="fe318-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="fe318-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe318-107">EXAMPLES</span></span>

### <span data-ttu-id="fe318-108">Пример 1. Создание объекта фильтра правила ManagementPolicy, его добавление в правило политики управления и настройка учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="fe318-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2 -BlobType appendBlob,blockBlob
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {appendBlob, blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="fe318-109">Эта команда создает объект фильтра правил ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="fe318-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="fe318-110">Затем добавьте его в правило политики управления и установите учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="fe318-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="fe318-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe318-111">PARAMETERS</span></span>

### <span data-ttu-id="fe318-112">-BlobType</span><span class="sxs-lookup"><span data-stu-id="fe318-112">-BlobType</span></span>
<span data-ttu-id="fe318-113">Массив строк для соития blobtypes.</span><span class="sxs-lookup"><span data-stu-id="fe318-113">An array of strings for blobtypes to be match.</span></span> <span data-ttu-id="fe318-114">В настоящее время blockBlob поддерживает все действия по удалите с уровня.</span><span class="sxs-lookup"><span data-stu-id="fe318-114">Currently blockBlob supports all tiering and delete actions.</span></span> <span data-ttu-id="fe318-115">Для приложения AppendBlob поддерживаются только действия удаления.</span><span class="sxs-lookup"><span data-stu-id="fe318-115">Only delete actions are supported for appendBlob.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: blockBlob, appendBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe318-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe318-116">-DefaultProfile</span></span>
<span data-ttu-id="fe318-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe318-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe318-118">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="fe318-118">-PrefixMatch</span></span>
<span data-ttu-id="fe318-119">Массив строк для совпадения префиксов.</span><span class="sxs-lookup"><span data-stu-id="fe318-119">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="fe318-120">Строка префикса должна начинаться с имени контейнера.</span><span class="sxs-lookup"><span data-stu-id="fe318-120">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="fe318-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe318-121">CommonParameters</span></span>
<span data-ttu-id="fe318-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe318-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe318-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe318-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe318-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe318-124">INPUTS</span></span>

### <span data-ttu-id="fe318-125">Нет</span><span class="sxs-lookup"><span data-stu-id="fe318-125">None</span></span>

## <span data-ttu-id="fe318-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe318-126">OUTPUTS</span></span>

### <span data-ttu-id="fe318-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="fe318-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="fe318-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe318-128">NOTES</span></span>

## <span data-ttu-id="fe318-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe318-129">RELATED LINKS</span></span>
