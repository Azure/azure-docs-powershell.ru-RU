---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244736"
---
# <span data-ttu-id="a04ff-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a04ff-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a04ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a04ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a04ff-103">Получение или перечисление связанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="a04ff-103">Get or list linked storage account</span></span>

## <span data-ttu-id="a04ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a04ff-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a04ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a04ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a04ff-106">Получение связанной учетной записи хранения, перечисление всех связанных учетных записей хранения, если не указан "-DataSourceType"</span><span class="sxs-lookup"><span data-stu-id="a04ff-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="a04ff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a04ff-107">EXAMPLES</span></span>

### <span data-ttu-id="a04ff-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a04ff-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="a04ff-109">список связанных хранилищ accoounts для рабочей области {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="a04ff-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="a04ff-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a04ff-110">PARAMETERS</span></span>

### <span data-ttu-id="a04ff-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="a04ff-111">-DataSourceType</span></span>
<span data-ttu-id="a04ff-112">Тип источника данных должен быть "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="a04ff-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04ff-113">-DefaultProfile</span></span>
<span data-ttu-id="a04ff-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a04ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a04ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="a04ff-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a04ff-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04ff-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a04ff-117">-WorkspaceName</span></span>
<span data-ttu-id="a04ff-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a04ff-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04ff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04ff-119">CommonParameters</span></span>
<span data-ttu-id="a04ff-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a04ff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04ff-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a04ff-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04ff-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a04ff-122">INPUTS</span></span>

### <span data-ttu-id="a04ff-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a04ff-123">System.String</span></span>

## <span data-ttu-id="a04ff-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a04ff-124">OUTPUTS</span></span>

### <span data-ttu-id="a04ff-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="a04ff-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="a04ff-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a04ff-126">NOTES</span></span>

## <span data-ttu-id="a04ff-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a04ff-127">RELATED LINKS</span></span>