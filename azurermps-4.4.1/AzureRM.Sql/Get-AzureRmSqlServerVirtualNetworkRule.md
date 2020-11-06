---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: e73409edf07402dd44cb5f29a6e878d29d7bfede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559475"
---
# <span data-ttu-id="4a6a7-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4a6a7-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="4a6a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6a7-103">Возвращает или перечисляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4a6a7-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a6a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a6a7-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a6a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a6a7-105">DESCRIPTION</span></span>
<span data-ttu-id="4a6a7-106">Эта команда возвращает конкретное правило виртуальной сети Azure SQL Server или список правил виртуальной сети Azure SQL Server на сервере.</span><span class="sxs-lookup"><span data-stu-id="4a6a7-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="4a6a7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a6a7-107">EXAMPLES</span></span>

### <span data-ttu-id="4a6a7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a6a7-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="4a6a7-109">Возвращает одно правило виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="4a6a7-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="4a6a7-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4a6a7-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="4a6a7-111">Получает список правил виртуальных сетей Azure SQL Server на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="4a6a7-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="4a6a7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a6a7-112">PARAMETERS</span></span>

### <span data-ttu-id="4a6a7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6a7-113">-ResourceGroupName</span></span>
<span data-ttu-id="4a6a7-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a6a7-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a6a7-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4a6a7-115">-ServerName</span></span>
<span data-ttu-id="4a6a7-116">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4a6a7-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4a6a7-117">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="4a6a7-117">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="4a6a7-118">Имя правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4a6a7-118">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="4a6a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6a7-119">-DefaultProfile</span></span>
<span data-ttu-id="4a6a7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a6a7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a6a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6a7-121">CommonParameters</span></span>
<span data-ttu-id="4a6a7-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a6a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6a7-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a6a7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6a7-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a6a7-124">INPUTS</span></span>

### <span data-ttu-id="4a6a7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4a6a7-125">System.String</span></span>

## <span data-ttu-id="4a6a7-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a6a7-126">OUTPUTS</span></span>

### <span data-ttu-id="4a6a7-127">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="4a6a7-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="4a6a7-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a6a7-128">NOTES</span></span>

## <span data-ttu-id="4a6a7-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a6a7-129">RELATED LINKS</span></span>

