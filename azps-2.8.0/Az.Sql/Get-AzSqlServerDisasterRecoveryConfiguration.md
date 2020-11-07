---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ac62ac0307422f0015fe578937a80a03e2a730d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906658"
---
# <span data-ttu-id="89bd5-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="89bd5-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="89bd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="89bd5-103">Возвращает конфигурацию восстановления системы сервера баз данных.</span><span class="sxs-lookup"><span data-stu-id="89bd5-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="89bd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89bd5-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89bd5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="89bd5-106">Командлет **Get-AzSqlServerDisasterRecoveryConfiguration** возвращает конфигурацию восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="89bd5-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="89bd5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89bd5-107">EXAMPLES</span></span>

## <span data-ttu-id="89bd5-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89bd5-108">PARAMETERS</span></span>

### <span data-ttu-id="89bd5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bd5-109">-DefaultProfile</span></span>
<span data-ttu-id="89bd5-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89bd5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89bd5-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89bd5-111">-ResourceGroupName</span></span>
<span data-ttu-id="89bd5-112">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89bd5-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="89bd5-113">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="89bd5-113">-ServerName</span></span>
<span data-ttu-id="89bd5-114">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="89bd5-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="89bd5-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="89bd5-115">-VirtualEndpointName</span></span>
<span data-ttu-id="89bd5-116">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="89bd5-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="89bd5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89bd5-117">-Confirm</span></span>
<span data-ttu-id="89bd5-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89bd5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89bd5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89bd5-119">-WhatIf</span></span>
<span data-ttu-id="89bd5-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89bd5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89bd5-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89bd5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89bd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bd5-122">CommonParameters</span></span>
<span data-ttu-id="89bd5-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89bd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bd5-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89bd5-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bd5-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89bd5-125">INPUTS</span></span>

### <span data-ttu-id="89bd5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="89bd5-126">System.String</span></span>

## <span data-ttu-id="89bd5-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89bd5-127">OUTPUTS</span></span>

### <span data-ttu-id="89bd5-128">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="89bd5-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="89bd5-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="89bd5-129">NOTES</span></span>

## <span data-ttu-id="89bd5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89bd5-130">RELATED LINKS</span></span>

[<span data-ttu-id="89bd5-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="89bd5-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="89bd5-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="89bd5-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="89bd5-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="89bd5-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="89bd5-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="89bd5-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

