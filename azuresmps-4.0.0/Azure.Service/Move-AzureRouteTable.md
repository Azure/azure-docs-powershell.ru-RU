---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076241"
---
# <span data-ttu-id="f63c0-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="f63c0-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="f63c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f63c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f63c0-103">Переносит таблицу маршрутов в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f63c0-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f63c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f63c0-104">SYNTAX</span></span>

### <span data-ttu-id="f63c0-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f63c0-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f63c0-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f63c0-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f63c0-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f63c0-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f63c0-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f63c0-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f63c0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f63c0-109">DESCRIPTION</span></span>
<span data-ttu-id="f63c0-110">Командлет **Move-AzureRouteTable** переносит таблицу маршрутов в группу ресурсов в стеке диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f63c0-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f63c0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f63c0-111">EXAMPLES</span></span>

### <span data-ttu-id="f63c0-112">1:</span><span class="sxs-lookup"><span data-stu-id="f63c0-112">1:</span></span>
```

```

## <span data-ttu-id="f63c0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f63c0-113">PARAMETERS</span></span>

### <span data-ttu-id="f63c0-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="f63c0-114">-Abort</span></span>
<span data-ttu-id="f63c0-115">Указывает, что этот командлет отменяет миграцию таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f63c0-115">Indicates that this cmdlet cancels the route table migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63c0-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="f63c0-116">-Commit</span></span>
<span data-ttu-id="f63c0-117">Указывает на то, что этот командлет запускает миграцию таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f63c0-117">Indicates that this cmdlet starts the route table migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63c0-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f63c0-118">-InformationAction</span></span>
<span data-ttu-id="f63c0-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f63c0-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f63c0-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f63c0-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f63c0-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f63c0-121">Continue</span></span>
- <span data-ttu-id="f63c0-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f63c0-122">Ignore</span></span>
- <span data-ttu-id="f63c0-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f63c0-123">Inquire</span></span>
- <span data-ttu-id="f63c0-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f63c0-124">SilentlyContinue</span></span>
- <span data-ttu-id="f63c0-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="f63c0-125">Stop</span></span>
- <span data-ttu-id="f63c0-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="f63c0-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63c0-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f63c0-127">-InformationVariable</span></span>
<span data-ttu-id="f63c0-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f63c0-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63c0-129">-Подготовка</span><span class="sxs-lookup"><span data-stu-id="f63c0-129">-Prepare</span></span>
<span data-ttu-id="f63c0-130">Указывает на то, что этот командлет подготавливает таблицу маршрутов для миграции.</span><span class="sxs-lookup"><span data-stu-id="f63c0-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63c0-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="f63c0-131">-Profile</span></span>
<span data-ttu-id="f63c0-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f63c0-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f63c0-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f63c0-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63c0-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="f63c0-134">-RouteTableName</span></span>
<span data-ttu-id="f63c0-135">Указывает имя таблицы маршрутов, которая переносится этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f63c0-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="f63c0-136">-Проверка</span><span class="sxs-lookup"><span data-stu-id="f63c0-136">-Validate</span></span>
<span data-ttu-id="f63c0-137">Указывает, что этот командлет проверяет таблицу маршрутов для миграции.</span><span class="sxs-lookup"><span data-stu-id="f63c0-137">Specifies that this cmdlet validates the route table for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63c0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f63c0-138">-Confirm</span></span>
<span data-ttu-id="f63c0-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f63c0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f63c0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f63c0-140">-WhatIf</span></span>
<span data-ttu-id="f63c0-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f63c0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f63c0-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f63c0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f63c0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63c0-143">CommonParameters</span></span>
<span data-ttu-id="f63c0-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f63c0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63c0-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f63c0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63c0-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f63c0-146">INPUTS</span></span>

## <span data-ttu-id="f63c0-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f63c0-147">OUTPUTS</span></span>

## <span data-ttu-id="f63c0-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f63c0-148">NOTES</span></span>

## <span data-ttu-id="f63c0-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f63c0-149">RELATED LINKS</span></span>

[<span data-ttu-id="f63c0-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f63c0-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="f63c0-151">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="f63c0-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="f63c0-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="f63c0-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="f63c0-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f63c0-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="f63c0-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f63c0-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


