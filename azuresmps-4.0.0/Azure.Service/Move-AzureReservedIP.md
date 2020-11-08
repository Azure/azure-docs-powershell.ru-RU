---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076242"
---
# <span data-ttu-id="14450-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="14450-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="14450-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14450-102">SYNOPSIS</span></span>
<span data-ttu-id="14450-103">Переносит зарезервированный IP-адрес в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="14450-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="14450-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14450-104">SYNTAX</span></span>

### <span data-ttu-id="14450-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="14450-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14450-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="14450-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14450-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="14450-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14450-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="14450-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14450-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14450-109">DESCRIPTION</span></span>
<span data-ttu-id="14450-110">Командлет **Move-AzureReservedIP** переносит зарезервированный IP-адрес в группу ресурсов в стеке диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="14450-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="14450-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14450-111">EXAMPLES</span></span>

### <span data-ttu-id="14450-112">1:</span><span class="sxs-lookup"><span data-stu-id="14450-112">1:</span></span>
```

```

## <span data-ttu-id="14450-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14450-113">PARAMETERS</span></span>

### <span data-ttu-id="14450-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="14450-114">-Abort</span></span>
<span data-ttu-id="14450-115">Указывает на то, что этот командлет отменяет зарезервированную миграцию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="14450-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

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

### <span data-ttu-id="14450-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="14450-116">-Commit</span></span>
<span data-ttu-id="14450-117">Указывает на то, что этот командлет запускает зарезервированную миграцию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="14450-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

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

### <span data-ttu-id="14450-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="14450-118">-InformationAction</span></span>
<span data-ttu-id="14450-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="14450-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="14450-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="14450-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="14450-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="14450-121">Continue</span></span>
- <span data-ttu-id="14450-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="14450-122">Ignore</span></span>
- <span data-ttu-id="14450-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="14450-123">Inquire</span></span>
- <span data-ttu-id="14450-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="14450-124">SilentlyContinue</span></span>
- <span data-ttu-id="14450-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="14450-125">Stop</span></span>
- <span data-ttu-id="14450-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="14450-126">Suspend</span></span>

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

### <span data-ttu-id="14450-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="14450-127">-InformationVariable</span></span>
<span data-ttu-id="14450-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="14450-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="14450-129">-Подготовка</span><span class="sxs-lookup"><span data-stu-id="14450-129">-Prepare</span></span>
<span data-ttu-id="14450-130">Указывает на то, что этот командлет подготавливает зарезервированный IP-адрес для миграции.</span><span class="sxs-lookup"><span data-stu-id="14450-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="14450-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="14450-131">-Profile</span></span>
<span data-ttu-id="14450-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="14450-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14450-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14450-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14450-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="14450-134">-ReservedIPName</span></span>
<span data-ttu-id="14450-135">Задает зарезервированный IP-адрес, на который переносится этот командлет.</span><span class="sxs-lookup"><span data-stu-id="14450-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="14450-136">-Проверка</span><span class="sxs-lookup"><span data-stu-id="14450-136">-Validate</span></span>
<span data-ttu-id="14450-137">Указывает, что этот командлет проверит зарезервированный IP-адрес для миграции.</span><span class="sxs-lookup"><span data-stu-id="14450-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="14450-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14450-138">-Confirm</span></span>
<span data-ttu-id="14450-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14450-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14450-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14450-140">-WhatIf</span></span>
<span data-ttu-id="14450-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14450-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14450-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14450-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14450-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14450-143">CommonParameters</span></span>
<span data-ttu-id="14450-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14450-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14450-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14450-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14450-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14450-146">INPUTS</span></span>

## <span data-ttu-id="14450-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14450-147">OUTPUTS</span></span>

## <span data-ttu-id="14450-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="14450-148">NOTES</span></span>

## <span data-ttu-id="14450-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14450-149">RELATED LINKS</span></span>

[<span data-ttu-id="14450-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="14450-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="14450-151">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="14450-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="14450-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="14450-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="14450-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14450-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="14450-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14450-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


