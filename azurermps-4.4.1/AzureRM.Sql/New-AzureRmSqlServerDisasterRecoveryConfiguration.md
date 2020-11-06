---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 06d0b7eae38459943872926b640a0f48b2e28b08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559443"
---
# <span data-ttu-id="2a56b-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a56b-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2a56b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a56b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a56b-103">Создает конфигурацию восстановления системы сервера баз данных.</span><span class="sxs-lookup"><span data-stu-id="2a56b-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a56b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a56b-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a56b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a56b-105">DESCRIPTION</span></span>
<span data-ttu-id="2a56b-106">Командлет **New-AzureRmSqlServerDisasterRecoveryConfiguration** создает конфигурацию восстановления системы для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2a56b-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2a56b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a56b-107">EXAMPLES</span></span>

## <span data-ttu-id="2a56b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a56b-108">PARAMETERS</span></span>

### <span data-ttu-id="2a56b-109">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="2a56b-109">-FailoverPolicy</span></span>
<span data-ttu-id="2a56b-110">Указывает политику перемещения при сбое.</span><span class="sxs-lookup"><span data-stu-id="2a56b-110">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="2a56b-111">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a56b-111">-PartnerResourceGroupName</span></span>
<span data-ttu-id="2a56b-112">Указывает имя группы ресурсов для партнеров.</span><span class="sxs-lookup"><span data-stu-id="2a56b-112">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="2a56b-113">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="2a56b-113">-PartnerServerName</span></span>
<span data-ttu-id="2a56b-114">Указывает имя сервера-партнера.</span><span class="sxs-lookup"><span data-stu-id="2a56b-114">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="2a56b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a56b-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a56b-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a56b-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2a56b-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2a56b-117">-ServerName</span></span>
<span data-ttu-id="2a56b-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2a56b-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2a56b-119">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2a56b-119">-VirtualEndpointName</span></span>
<span data-ttu-id="2a56b-120">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2a56b-120">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="2a56b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a56b-121">-Confirm</span></span>
<span data-ttu-id="2a56b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a56b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a56b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a56b-123">-WhatIf</span></span>
<span data-ttu-id="2a56b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a56b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a56b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a56b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a56b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a56b-126">-DefaultProfile</span></span>
<span data-ttu-id="2a56b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a56b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a56b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a56b-128">CommonParameters</span></span>
<span data-ttu-id="2a56b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a56b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a56b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a56b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a56b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a56b-131">INPUTS</span></span>

## <span data-ttu-id="2a56b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a56b-132">OUTPUTS</span></span>

## <span data-ttu-id="2a56b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a56b-133">NOTES</span></span>

## <span data-ttu-id="2a56b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a56b-134">RELATED LINKS</span></span>

[<span data-ttu-id="2a56b-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a56b-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2a56b-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a56b-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2a56b-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a56b-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2a56b-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2a56b-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
