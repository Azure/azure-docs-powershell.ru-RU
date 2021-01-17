---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392511"
---
# <span data-ttu-id="05b4d-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="05b4d-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="05b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="05b4d-103">Получает или перечисляет правило виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="05b4d-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="05b4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05b4d-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05b4d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="05b4d-106">Эта команда получает определенное правило виртуальной SQL Server Azure SQL Server или список правил виртуальной сети Azure SQL Server под сервером.</span><span class="sxs-lookup"><span data-stu-id="05b4d-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="05b4d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05b4d-107">EXAMPLES</span></span>

### <span data-ttu-id="05b4d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05b4d-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="05b4d-109">Получает одно правило виртуальной SQL Server Azure</span><span class="sxs-lookup"><span data-stu-id="05b4d-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="05b4d-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="05b4d-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="05b4d-111">Получает список правил виртуальной SQL Server Azure для сети, которые находятся под указанным сервером</span><span class="sxs-lookup"><span data-stu-id="05b4d-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="05b4d-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="05b4d-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="05b4d-113">Список правил виртуальной сети Azure SQL Server под указанным сервером, который начинается с virtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="05b4d-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="05b4d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05b4d-114">PARAMETERS</span></span>

### <span data-ttu-id="05b4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b4d-115">-DefaultProfile</span></span>
<span data-ttu-id="05b4d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="05b4d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05b4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="05b4d-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05b4d-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05b4d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05b4d-119">-ServerName</span></span>
<span data-ttu-id="05b4d-120">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="05b4d-120">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b4d-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="05b4d-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="05b4d-122">Имя правила виртуальной сети Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="05b4d-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b4d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b4d-123">CommonParameters</span></span>
<span data-ttu-id="05b4d-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05b4d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b4d-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05b4d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b4d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05b4d-126">INPUTS</span></span>

### <span data-ttu-id="05b4d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="05b4d-127">System.String</span></span>

## <span data-ttu-id="05b4d-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05b4d-128">OUTPUTS</span></span>

### <span data-ttu-id="05b4d-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="05b4d-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="05b4d-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05b4d-130">NOTES</span></span>

## <span data-ttu-id="05b4d-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05b4d-131">RELATED LINKS</span></span>
