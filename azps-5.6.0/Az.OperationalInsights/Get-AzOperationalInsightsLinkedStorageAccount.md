---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ae174f31cdbe23a28dd9a21b44b640239e78fdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976499"
---
# <span data-ttu-id="16b93-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="16b93-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="16b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16b93-102">SYNOPSIS</span></span>
<span data-ttu-id="16b93-103">Получить или перечислить связанную учетную запись хранения</span><span class="sxs-lookup"><span data-stu-id="16b93-103">Get or list linked storage account</span></span>

## <span data-ttu-id="16b93-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16b93-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16b93-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16b93-105">DESCRIPTION</span></span>
<span data-ttu-id="16b93-106">Получить связанную учетную запись хранения, перечислить все связанные учетные записи хранения, если не указан "-DataSourceType"</span><span class="sxs-lookup"><span data-stu-id="16b93-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="16b93-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16b93-107">EXAMPLES</span></span>

### <span data-ttu-id="16b93-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16b93-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="16b93-109">список связанных accoounts хранилища для рабочей области {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="16b93-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="16b93-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16b93-110">PARAMETERS</span></span>

### <span data-ttu-id="16b93-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="16b93-111">-DataSourceType</span></span>
<span data-ttu-id="16b93-112">Тип источника данных должен быть одним из типов CustomLogs и AzureWatson.</span><span class="sxs-lookup"><span data-stu-id="16b93-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="16b93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b93-113">-DefaultProfile</span></span>
<span data-ttu-id="16b93-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16b93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b93-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b93-115">-ResourceGroupName</span></span>
<span data-ttu-id="16b93-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16b93-116">The resource group name.</span></span>

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

### <span data-ttu-id="16b93-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="16b93-117">-WorkspaceName</span></span>
<span data-ttu-id="16b93-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="16b93-118">The workspace name.</span></span>

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

### <span data-ttu-id="16b93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b93-119">CommonParameters</span></span>
<span data-ttu-id="16b93-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b93-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16b93-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b93-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16b93-122">INPUTS</span></span>

### <span data-ttu-id="16b93-123">System.String</span><span class="sxs-lookup"><span data-stu-id="16b93-123">System.String</span></span>

## <span data-ttu-id="16b93-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16b93-124">OUTPUTS</span></span>

### <span data-ttu-id="16b93-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="16b93-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="16b93-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16b93-126">NOTES</span></span>

## <span data-ttu-id="16b93-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16b93-127">RELATED LINKS</span></span>