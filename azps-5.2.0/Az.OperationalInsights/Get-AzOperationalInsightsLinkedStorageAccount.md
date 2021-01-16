---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401660"
---
# <span data-ttu-id="c561a-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c561a-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="c561a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c561a-102">SYNOPSIS</span></span>
<span data-ttu-id="c561a-103">Получить или перечислить связанную учетную запись хранения</span><span class="sxs-lookup"><span data-stu-id="c561a-103">Get or list linked storage account</span></span>

## <span data-ttu-id="c561a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c561a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c561a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c561a-105">DESCRIPTION</span></span>
<span data-ttu-id="c561a-106">Получить связанную учетную запись хранения, перечислить все связанные учетные записи хранения, если не указан "-DataSourceType"</span><span class="sxs-lookup"><span data-stu-id="c561a-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="c561a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c561a-107">EXAMPLES</span></span>

### <span data-ttu-id="c561a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c561a-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="c561a-109">список связанных accoounts хранилища для рабочей области {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="c561a-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="c561a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c561a-110">PARAMETERS</span></span>

### <span data-ttu-id="c561a-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="c561a-111">-DataSourceType</span></span>
<span data-ttu-id="c561a-112">Тип источника данных должен быть одним из типов CustomLogs и AzureWatson.</span><span class="sxs-lookup"><span data-stu-id="c561a-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="c561a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c561a-113">-DefaultProfile</span></span>
<span data-ttu-id="c561a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c561a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c561a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c561a-115">-ResourceGroupName</span></span>
<span data-ttu-id="c561a-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c561a-116">The resource group name.</span></span>

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

### <span data-ttu-id="c561a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c561a-117">-WorkspaceName</span></span>
<span data-ttu-id="c561a-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c561a-118">The workspace name.</span></span>

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

### <span data-ttu-id="c561a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c561a-119">CommonParameters</span></span>
<span data-ttu-id="c561a-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c561a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c561a-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c561a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c561a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c561a-122">INPUTS</span></span>

### <span data-ttu-id="c561a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c561a-123">System.String</span></span>

## <span data-ttu-id="c561a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c561a-124">OUTPUTS</span></span>

### <span data-ttu-id="c561a-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="c561a-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="c561a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c561a-126">NOTES</span></span>

## <span data-ttu-id="c561a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c561a-127">RELATED LINKS</span></span>