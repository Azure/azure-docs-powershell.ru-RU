---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 3e9b99a1ab9d3fdce813166e7a0834c14b81b651
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728924"
---
# <span data-ttu-id="476ff-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="476ff-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="476ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="476ff-102">SYNOPSIS</span></span>
<span data-ttu-id="476ff-103">Возвращает или перечисляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="476ff-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="476ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="476ff-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="476ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="476ff-105">DESCRIPTION</span></span>
<span data-ttu-id="476ff-106">Эта команда возвращает конкретное правило виртуальной сети Azure SQL Server или список правил виртуальной сети Azure SQL Server на сервере.</span><span class="sxs-lookup"><span data-stu-id="476ff-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="476ff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="476ff-107">EXAMPLES</span></span>

### <span data-ttu-id="476ff-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="476ff-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="476ff-109">Возвращает одно правило виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="476ff-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="476ff-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="476ff-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="476ff-111">Получает список правил виртуальных сетей Azure SQL Server на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="476ff-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="476ff-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="476ff-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="476ff-113">Получает список правил виртуальных сетей Azure SQL Server на указанном сервере, который начинается с "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="476ff-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="476ff-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="476ff-114">PARAMETERS</span></span>

### <span data-ttu-id="476ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476ff-115">-DefaultProfile</span></span>
<span data-ttu-id="476ff-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="476ff-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="476ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="476ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="476ff-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="476ff-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="476ff-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="476ff-119">-ServerName</span></span>
<span data-ttu-id="476ff-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="476ff-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="476ff-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="476ff-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="476ff-122">Имя правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="476ff-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="476ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476ff-123">CommonParameters</span></span>
<span data-ttu-id="476ff-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="476ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476ff-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="476ff-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476ff-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="476ff-126">INPUTS</span></span>

### <span data-ttu-id="476ff-127">System. String</span><span class="sxs-lookup"><span data-stu-id="476ff-127">System.String</span></span>

## <span data-ttu-id="476ff-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="476ff-128">OUTPUTS</span></span>

### <span data-ttu-id="476ff-129">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="476ff-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="476ff-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="476ff-130">NOTES</span></span>

## <span data-ttu-id="476ff-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="476ff-131">RELATED LINKS</span></span>
