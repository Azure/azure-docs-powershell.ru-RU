---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073912"
---
# <span data-ttu-id="bcfa8-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcfa8-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="bcfa8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcfa8-102">SYNOPSIS</span></span>
<span data-ttu-id="bcfa8-103">Возвращает конфигурацию восстановления системы сервера баз данных.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="bcfa8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcfa8-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcfa8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcfa8-105">DESCRIPTION</span></span>
<span data-ttu-id="bcfa8-106">Командлет **Get-AzSqlServerDisasterRecoveryConfiguration** возвращает конфигурацию восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="bcfa8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcfa8-107">EXAMPLES</span></span>

## <span data-ttu-id="bcfa8-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcfa8-108">PARAMETERS</span></span>

### <span data-ttu-id="bcfa8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcfa8-109">-DefaultProfile</span></span>
<span data-ttu-id="bcfa8-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bcfa8-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcfa8-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcfa8-111">-ResourceGroupName</span></span>
<span data-ttu-id="bcfa8-112">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bcfa8-113">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bcfa8-113">-ServerName</span></span>
<span data-ttu-id="bcfa8-114">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="bcfa8-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="bcfa8-115">-VirtualEndpointName</span></span>
<span data-ttu-id="bcfa8-116">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="bcfa8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcfa8-117">-Confirm</span></span>
<span data-ttu-id="bcfa8-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcfa8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcfa8-119">-WhatIf</span></span>
<span data-ttu-id="bcfa8-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcfa8-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcfa8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcfa8-122">CommonParameters</span></span>
<span data-ttu-id="bcfa8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcfa8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcfa8-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcfa8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcfa8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcfa8-125">INPUTS</span></span>

### <span data-ttu-id="bcfa8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bcfa8-126">System.String</span></span>

## <span data-ttu-id="bcfa8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcfa8-127">OUTPUTS</span></span>

### <span data-ttu-id="bcfa8-128">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="bcfa8-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="bcfa8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcfa8-129">NOTES</span></span>

## <span data-ttu-id="bcfa8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcfa8-130">RELATED LINKS</span></span>

[<span data-ttu-id="bcfa8-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcfa8-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="bcfa8-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcfa8-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="bcfa8-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcfa8-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="bcfa8-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="bcfa8-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

