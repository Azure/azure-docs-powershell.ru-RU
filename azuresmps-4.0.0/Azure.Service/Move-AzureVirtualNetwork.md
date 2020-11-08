---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076238"
---
# <span data-ttu-id="c6577-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c6577-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="c6577-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6577-102">SYNOPSIS</span></span>
<span data-ttu-id="c6577-103">Переносит виртуальную сеть в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c6577-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c6577-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6577-104">SYNTAX</span></span>

### <span data-ttu-id="c6577-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6577-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6577-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6577-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6577-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6577-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6577-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6577-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6577-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6577-109">DESCRIPTION</span></span>
<span data-ttu-id="c6577-110">Командлет **Move-AzureVirtualNetwork** переносит виртуальную сеть в группу ресурсов в стеке диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c6577-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c6577-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6577-111">EXAMPLES</span></span>

### <span data-ttu-id="c6577-112">Пример 1: подготовка миграции виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="c6577-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="c6577-113">Эта команда подготавливает виртуальную сеть с именем ContosoVNET для миграции в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c6577-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="c6577-114">Пример 2: начало миграции виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="c6577-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="c6577-115">Эта команда запускает миграцию виртуальной сети с именем ContosoVNET в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c6577-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="c6577-116">Пример 3: Проверка миграции виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="c6577-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="c6577-117">Эта команда проверяет миграцию виртуальной сети с именем ContosoVNET в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c6577-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c6577-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6577-118">PARAMETERS</span></span>

### <span data-ttu-id="c6577-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="c6577-119">-Abort</span></span>
<span data-ttu-id="c6577-120">Указывает, что этот командлет отменяет миграцию виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c6577-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

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

### <span data-ttu-id="c6577-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="c6577-121">-Commit</span></span>
<span data-ttu-id="c6577-122">Указывает на то, что этот командлет запускает миграцию виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c6577-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

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

### <span data-ttu-id="c6577-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c6577-123">-InformationAction</span></span>
<span data-ttu-id="c6577-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c6577-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c6577-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c6577-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6577-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c6577-126">Continue</span></span>
- <span data-ttu-id="c6577-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c6577-127">Ignore</span></span>
- <span data-ttu-id="c6577-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c6577-128">Inquire</span></span>
- <span data-ttu-id="c6577-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c6577-129">SilentlyContinue</span></span>
- <span data-ttu-id="c6577-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="c6577-130">Stop</span></span>
- <span data-ttu-id="c6577-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="c6577-131">Suspend</span></span>

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

### <span data-ttu-id="c6577-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c6577-132">-InformationVariable</span></span>
<span data-ttu-id="c6577-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c6577-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c6577-134">-Подготовка</span><span class="sxs-lookup"><span data-stu-id="c6577-134">-Prepare</span></span>
<span data-ttu-id="c6577-135">Указывает, что этот командлет подготавливает виртуальную сеть для миграции.</span><span class="sxs-lookup"><span data-stu-id="c6577-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

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

### <span data-ttu-id="c6577-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="c6577-136">-Profile</span></span>
<span data-ttu-id="c6577-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c6577-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6577-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6577-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6577-139">-Проверка</span><span class="sxs-lookup"><span data-stu-id="c6577-139">-Validate</span></span>
<span data-ttu-id="c6577-140">Указывает, что этот командлет проверяет виртуальную сеть для миграции.</span><span class="sxs-lookup"><span data-stu-id="c6577-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

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

### <span data-ttu-id="c6577-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c6577-141">-VirtualNetworkName</span></span>
<span data-ttu-id="c6577-142">Имя виртуальной сети для миграции</span><span class="sxs-lookup"><span data-stu-id="c6577-142">Name of the Virtual Network to migrate</span></span>

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

### <span data-ttu-id="c6577-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6577-143">-Confirm</span></span>
<span data-ttu-id="c6577-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6577-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6577-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6577-145">-WhatIf</span></span>
<span data-ttu-id="c6577-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6577-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6577-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6577-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6577-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6577-148">CommonParameters</span></span>
<span data-ttu-id="c6577-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6577-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6577-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6577-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6577-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6577-151">INPUTS</span></span>

## <span data-ttu-id="c6577-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6577-152">OUTPUTS</span></span>

## <span data-ttu-id="c6577-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6577-153">NOTES</span></span>

## <span data-ttu-id="c6577-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6577-154">RELATED LINKS</span></span>

[<span data-ttu-id="c6577-155">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6577-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="c6577-156">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="c6577-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="c6577-157">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6577-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="c6577-158">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="c6577-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="c6577-159">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6577-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


