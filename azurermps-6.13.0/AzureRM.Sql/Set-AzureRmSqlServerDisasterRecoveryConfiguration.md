---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 19f7d8adf7e8eae48bb85c19c9f01c61dc741da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562563"
---
# <span data-ttu-id="af343-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="af343-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="af343-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af343-102">SYNOPSIS</span></span>
<span data-ttu-id="af343-103">Изменяет конфигурацию восстановления сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="af343-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af343-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af343-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af343-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af343-105">DESCRIPTION</span></span>
<span data-ttu-id="af343-106">Командлет **Set-AzureRmSqlServerDisasterRecoveryConfiguration** изменяет конфигурацию восстановления сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="af343-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="af343-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af343-107">EXAMPLES</span></span>

## <span data-ttu-id="af343-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af343-108">PARAMETERS</span></span>

### <span data-ttu-id="af343-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="af343-109">-AllowDataLoss</span></span>
<span data-ttu-id="af343-110">Указывает на то, что операция отработки отказа допускает потерю данных.</span><span class="sxs-lookup"><span data-stu-id="af343-110">Indicates that the failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af343-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af343-111">-AsJob</span></span>
<span data-ttu-id="af343-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="af343-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af343-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af343-113">-DefaultProfile</span></span>
<span data-ttu-id="af343-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="af343-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af343-115">-Отработка отказа</span><span class="sxs-lookup"><span data-stu-id="af343-115">-Failover</span></span>
<span data-ttu-id="af343-116">Указывает на то, что эта операция является отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="af343-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af343-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af343-117">-ResourceGroupName</span></span>
<span data-ttu-id="af343-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af343-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="af343-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="af343-119">-ServerName</span></span>
<span data-ttu-id="af343-120">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="af343-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="af343-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="af343-121">-VirtualEndpointName</span></span>
<span data-ttu-id="af343-122">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="af343-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="af343-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af343-123">-Confirm</span></span>
<span data-ttu-id="af343-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af343-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af343-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af343-125">-WhatIf</span></span>
<span data-ttu-id="af343-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af343-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af343-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af343-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af343-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af343-128">CommonParameters</span></span>
<span data-ttu-id="af343-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af343-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af343-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af343-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af343-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af343-131">INPUTS</span></span>

### <span data-ttu-id="af343-132">System. String</span><span class="sxs-lookup"><span data-stu-id="af343-132">System.String</span></span>

## <span data-ttu-id="af343-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af343-133">OUTPUTS</span></span>

### <span data-ttu-id="af343-134">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="af343-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="af343-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="af343-135">NOTES</span></span>

## <span data-ttu-id="af343-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af343-136">RELATED LINKS</span></span>

[<span data-ttu-id="af343-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="af343-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="af343-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="af343-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="af343-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="af343-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="af343-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="af343-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
