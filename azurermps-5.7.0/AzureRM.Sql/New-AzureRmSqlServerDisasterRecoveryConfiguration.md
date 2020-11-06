---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566070"
---
# <span data-ttu-id="ba060-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba060-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="ba060-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba060-102">SYNOPSIS</span></span>
<span data-ttu-id="ba060-103">Создает конфигурацию восстановления системы сервера баз данных.</span><span class="sxs-lookup"><span data-stu-id="ba060-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba060-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba060-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba060-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba060-105">DESCRIPTION</span></span>
<span data-ttu-id="ba060-106">Командлет **New-AzureRmSqlServerDisasterRecoveryConfiguration** создает конфигурацию восстановления системы для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ba060-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ba060-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba060-107">EXAMPLES</span></span>

## <span data-ttu-id="ba060-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba060-108">PARAMETERS</span></span>

### <span data-ttu-id="ba060-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba060-109">-AsJob</span></span>
<span data-ttu-id="ba060-110">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ba060-110">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba060-111">-DefaultProfile</span></span>
<span data-ttu-id="ba060-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba060-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ba060-113">-FailoverPolicy</span></span>
<span data-ttu-id="ba060-114">Указывает политику перемещения при сбое.</span><span class="sxs-lookup"><span data-stu-id="ba060-114">Specifies the failover policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba060-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ba060-116">Указывает имя группы ресурсов для партнеров.</span><span class="sxs-lookup"><span data-stu-id="ba060-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ba060-117">-PartnerServerName</span></span>
<span data-ttu-id="ba060-118">Указывает имя сервера-партнера.</span><span class="sxs-lookup"><span data-stu-id="ba060-118">Specifies the name of the partner server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba060-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba060-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba060-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ba060-121">-ServerName</span></span>
<span data-ttu-id="ba060-122">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ba060-122">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="ba060-123">-VirtualEndpointName</span></span>
<span data-ttu-id="ba060-124">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ba060-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba060-125">-Confirm</span></span>
<span data-ttu-id="ba060-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba060-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba060-127">-WhatIf</span></span>
<span data-ttu-id="ba060-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba060-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba060-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba060-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba060-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba060-130">CommonParameters</span></span>
<span data-ttu-id="ba060-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba060-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba060-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba060-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba060-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba060-133">INPUTS</span></span>

### <span data-ttu-id="ba060-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="ba060-134">None</span></span>
<span data-ttu-id="ba060-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ba060-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba060-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba060-136">OUTPUTS</span></span>

## <span data-ttu-id="ba060-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba060-137">NOTES</span></span>

## <span data-ttu-id="ba060-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba060-138">RELATED LINKS</span></span>

[<span data-ttu-id="ba060-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba060-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ba060-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba060-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ba060-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba060-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ba060-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="ba060-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
