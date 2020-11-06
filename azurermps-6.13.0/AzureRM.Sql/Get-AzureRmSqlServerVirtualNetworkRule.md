---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 68fb8bac3a492bec915af6aea7df5d67fc3668dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558232"
---
# <span data-ttu-id="472ea-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="472ea-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="472ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="472ea-102">SYNOPSIS</span></span>
<span data-ttu-id="472ea-103">Возвращает или перечисляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="472ea-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="472ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="472ea-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="472ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="472ea-105">DESCRIPTION</span></span>
<span data-ttu-id="472ea-106">Эта команда возвращает конкретное правило виртуальной сети Azure SQL Server или список правил виртуальной сети Azure SQL Server на сервере.</span><span class="sxs-lookup"><span data-stu-id="472ea-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="472ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="472ea-107">EXAMPLES</span></span>

### <span data-ttu-id="472ea-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="472ea-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="472ea-109">Возвращает одно правило виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="472ea-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="472ea-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="472ea-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="472ea-111">Получает список правил виртуальных сетей Azure SQL Server на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="472ea-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="472ea-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="472ea-112">PARAMETERS</span></span>

### <span data-ttu-id="472ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472ea-113">-DefaultProfile</span></span>
<span data-ttu-id="472ea-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="472ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="472ea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="472ea-115">-ResourceGroupName</span></span>
<span data-ttu-id="472ea-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="472ea-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="472ea-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="472ea-117">-ServerName</span></span>
<span data-ttu-id="472ea-118">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="472ea-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="472ea-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="472ea-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="472ea-120">Имя правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="472ea-120">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="472ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472ea-121">CommonParameters</span></span>
<span data-ttu-id="472ea-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="472ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472ea-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="472ea-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472ea-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="472ea-124">INPUTS</span></span>

### <span data-ttu-id="472ea-125">System. String</span><span class="sxs-lookup"><span data-stu-id="472ea-125">System.String</span></span>

## <span data-ttu-id="472ea-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="472ea-126">OUTPUTS</span></span>

### <span data-ttu-id="472ea-127">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="472ea-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="472ea-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="472ea-128">NOTES</span></span>

## <span data-ttu-id="472ea-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="472ea-129">RELATED LINKS</span></span>
