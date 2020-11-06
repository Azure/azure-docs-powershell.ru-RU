---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 588954527c76bb0f5394afe4df9e19b37c10fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558788"
---
# <span data-ttu-id="53e40-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e40-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="53e40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53e40-102">SYNOPSIS</span></span>
<span data-ttu-id="53e40-103">Изменяет конфигурацию восстановления сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="53e40-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53e40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53e40-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53e40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53e40-105">DESCRIPTION</span></span>
<span data-ttu-id="53e40-106">Командлет **Set-AzureRmSqlServerDisasterRecoveryConfiguration** изменяет конфигурацию восстановления сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="53e40-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="53e40-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53e40-107">EXAMPLES</span></span>

## <span data-ttu-id="53e40-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53e40-108">PARAMETERS</span></span>

### <span data-ttu-id="53e40-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="53e40-109">-AllowDataLoss</span></span>
<span data-ttu-id="53e40-110">Указывает на то, что операция отработки отказа допускает потерю данных.</span><span class="sxs-lookup"><span data-stu-id="53e40-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="53e40-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53e40-111">-AsJob</span></span>
<span data-ttu-id="53e40-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="53e40-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e40-113">-DefaultProfile</span></span>
<span data-ttu-id="53e40-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="53e40-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53e40-115">-Отработка отказа</span><span class="sxs-lookup"><span data-stu-id="53e40-115">-Failover</span></span>
<span data-ttu-id="53e40-116">Указывает на то, что эта операция является отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="53e40-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e40-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53e40-117">-ResourceGroupName</span></span>
<span data-ttu-id="53e40-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53e40-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="53e40-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="53e40-119">-ServerName</span></span>
<span data-ttu-id="53e40-120">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="53e40-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="53e40-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="53e40-121">-VirtualEndpointName</span></span>
<span data-ttu-id="53e40-122">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="53e40-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="53e40-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53e40-123">-Confirm</span></span>
<span data-ttu-id="53e40-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="53e40-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53e40-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53e40-125">-WhatIf</span></span>
<span data-ttu-id="53e40-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="53e40-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53e40-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="53e40-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53e40-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e40-128">CommonParameters</span></span>
<span data-ttu-id="53e40-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53e40-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e40-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53e40-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e40-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53e40-131">INPUTS</span></span>

### <span data-ttu-id="53e40-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="53e40-132">None</span></span>
<span data-ttu-id="53e40-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="53e40-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53e40-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53e40-134">OUTPUTS</span></span>

## <span data-ttu-id="53e40-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="53e40-135">NOTES</span></span>

## <span data-ttu-id="53e40-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53e40-136">RELATED LINKS</span></span>

[<span data-ttu-id="53e40-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e40-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="53e40-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e40-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="53e40-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e40-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="53e40-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="53e40-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
