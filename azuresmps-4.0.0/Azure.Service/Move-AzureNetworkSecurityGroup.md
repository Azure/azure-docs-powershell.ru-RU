---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076243"
---
# <span data-ttu-id="6ce96-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6ce96-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="6ce96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ce96-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce96-103">Переносит группу безопасности сети в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce96-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="6ce96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ce96-104">SYNTAX</span></span>

### <span data-ttu-id="6ce96-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ce96-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ce96-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ce96-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ce96-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ce96-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ce96-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ce96-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ce96-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ce96-109">DESCRIPTION</span></span>
<span data-ttu-id="6ce96-110">Командлет **Move-AzureNetworkSecurityGroup** переносит группу безопасности сети в группу ресурсов в стеке диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce96-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="6ce96-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ce96-111">EXAMPLES</span></span>

### <span data-ttu-id="6ce96-112">1:</span><span class="sxs-lookup"><span data-stu-id="6ce96-112">1:</span></span>
```

```

## <span data-ttu-id="6ce96-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ce96-113">PARAMETERS</span></span>

### <span data-ttu-id="6ce96-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="6ce96-114">-Abort</span></span>
<span data-ttu-id="6ce96-115">Указывает, что этот командлет отменяет миграцию сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6ce96-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="6ce96-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="6ce96-116">-Commit</span></span>
<span data-ttu-id="6ce96-117">Указывает на то, что этот командлет запускает миграцию сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6ce96-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="6ce96-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6ce96-118">-InformationAction</span></span>
<span data-ttu-id="6ce96-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6ce96-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6ce96-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6ce96-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ce96-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6ce96-121">Continue</span></span>
- <span data-ttu-id="6ce96-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6ce96-122">Ignore</span></span>
- <span data-ttu-id="6ce96-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6ce96-123">Inquire</span></span>
- <span data-ttu-id="6ce96-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6ce96-124">SilentlyContinue</span></span>
- <span data-ttu-id="6ce96-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="6ce96-125">Stop</span></span>
- <span data-ttu-id="6ce96-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="6ce96-126">Suspend</span></span>

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

### <span data-ttu-id="6ce96-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6ce96-127">-InformationVariable</span></span>
<span data-ttu-id="6ce96-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6ce96-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6ce96-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce96-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="6ce96-130">Указывает имя группы безопасности сети, на которую переносится этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6ce96-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="6ce96-131">-Подготовка</span><span class="sxs-lookup"><span data-stu-id="6ce96-131">-Prepare</span></span>
<span data-ttu-id="6ce96-132">Указывает на то, что этот командлет подготавливает группу безопасности сети для миграции.</span><span class="sxs-lookup"><span data-stu-id="6ce96-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="6ce96-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ce96-133">-Profile</span></span>
<span data-ttu-id="6ce96-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6ce96-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ce96-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ce96-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ce96-136">-Проверка</span><span class="sxs-lookup"><span data-stu-id="6ce96-136">-Validate</span></span>
<span data-ttu-id="6ce96-137">Указывает, что этот командлет проверяет сетевую группу безопасности для миграции.</span><span class="sxs-lookup"><span data-stu-id="6ce96-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="6ce96-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ce96-138">-Confirm</span></span>
<span data-ttu-id="6ce96-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ce96-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce96-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce96-140">-WhatIf</span></span>
<span data-ttu-id="6ce96-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ce96-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce96-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ce96-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce96-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce96-143">CommonParameters</span></span>
<span data-ttu-id="6ce96-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ce96-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce96-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce96-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce96-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ce96-146">INPUTS</span></span>

## <span data-ttu-id="6ce96-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ce96-147">OUTPUTS</span></span>

## <span data-ttu-id="6ce96-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ce96-148">NOTES</span></span>

## <span data-ttu-id="6ce96-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ce96-149">RELATED LINKS</span></span>

[<span data-ttu-id="6ce96-150">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="6ce96-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="6ce96-151">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ce96-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="6ce96-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="6ce96-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="6ce96-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ce96-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="6ce96-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ce96-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


