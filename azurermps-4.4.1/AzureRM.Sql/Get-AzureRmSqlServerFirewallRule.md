---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 27715ee03871c08c53380861e2cd54d843b2ba51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733604"
---
# <span data-ttu-id="d8621-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8621-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="d8621-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8621-102">SYNOPSIS</span></span>
<span data-ttu-id="d8621-103">Возвращает правила брандмауэра для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d8621-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8621-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8621-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8621-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8621-105">DESCRIPTION</span></span>
<span data-ttu-id="d8621-106">Командлет **Get-AzureRmSqlServerFirewallRule** получает правила брандмауэра для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d8621-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="d8621-107">Если вы задаете имя правила брандмауэра, этот командлет получает сведения о конкретном правиле брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d8621-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="d8621-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8621-108">EXAMPLES</span></span>

### <span data-ttu-id="d8621-109">Пример 1: получение всех правил для сервера</span><span class="sxs-lookup"><span data-stu-id="d8621-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="d8621-110">Эта команда получает все правила брандмауэра для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="d8621-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="d8621-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8621-111">PARAMETERS</span></span>

### <span data-ttu-id="d8621-112">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="d8621-112">-FirewallRuleName</span></span>
<span data-ttu-id="d8621-113">Указывает имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d8621-113">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8621-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8621-114">-ResourceGroupName</span></span>
<span data-ttu-id="d8621-115">Указывает имя группы ресурсов, которой назначен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8621-115">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="d8621-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d8621-116">-ServerName</span></span>
<span data-ttu-id="d8621-117">Указывает имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8621-117">Specifies the name of the SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8621-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8621-118">-Confirm</span></span>
<span data-ttu-id="d8621-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8621-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8621-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8621-120">-WhatIf</span></span>
<span data-ttu-id="d8621-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8621-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8621-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8621-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8621-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8621-123">-DefaultProfile</span></span>
<span data-ttu-id="d8621-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8621-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8621-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8621-125">CommonParameters</span></span>
<span data-ttu-id="d8621-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8621-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8621-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8621-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8621-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8621-128">INPUTS</span></span>

## <span data-ttu-id="d8621-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8621-129">OUTPUTS</span></span>

### <span data-ttu-id="d8621-130">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="d8621-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="d8621-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8621-131">NOTES</span></span>

## <span data-ttu-id="d8621-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8621-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8621-133">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8621-133">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d8621-134">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8621-134">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d8621-135">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8621-135">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d8621-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="d8621-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


