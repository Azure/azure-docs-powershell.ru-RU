---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077411"
---
# <span data-ttu-id="5f863-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="5f863-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="5f863-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f863-102">SYNOPSIS</span></span>
<span data-ttu-id="5f863-103">Удаляет объекты роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5f863-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="5f863-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f863-104">SYNTAX</span></span>

### <span data-ttu-id="5f863-105">FromVMRoleObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f863-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f863-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="5f863-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f863-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f863-107">DESCRIPTION</span></span>
<span data-ttu-id="5f863-108">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="5f863-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5f863-109">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f863-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5f863-110">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5f863-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5f863-111">Командлет **Remove-WAPackVMRole** удаляет объекты роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5f863-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="5f863-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f863-112">EXAMPLES</span></span>

### <span data-ttu-id="5f863-113">Пример 1: Удаление роли виртуальной машины (созданной с помощью портала WAP)</span><span class="sxs-lookup"><span data-stu-id="5f863-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="5f863-114">Первая команда получает роль виртуальной машины с именем ContosoVMRole01 с помощью командлета **Get-WAPackVMRole** , а затем сохраняет этот объект в переменной $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5f863-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="5f863-115">Вторая команда удаляет роль виртуальной машины, хранящуюся в $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5f863-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="5f863-116">В командной строке появится запрос на подтверждение. Если вы предполагают, что эта роль виртуальной машины была создана с помощью портала WAP, вам не нужно указывать имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="5f863-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="5f863-117">Пример 2: Удаление роли виртуальной машины, созданной после создания облачной службы вручную</span><span class="sxs-lookup"><span data-stu-id="5f863-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="5f863-118">Первая команда получает роль виртуальной машины с именем "ContosoVMRole02" с помощью командлета **Get-WAPackVMRole** , а затем сохраняет этот объект в переменной $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5f863-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="5f863-119">Вторая команда удаляет роль виртуальной машины, хранящуюся в $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5f863-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="5f863-120">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5f863-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="5f863-121">Если вы предполагают, что эта роль виртуальной машины не была создана с помощью портала, пользователю необходимо указать имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="5f863-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="5f863-122">В этом случае с именем "ContosoCloudService02".</span><span class="sxs-lookup"><span data-stu-id="5f863-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="5f863-123">Пример 3: Удаление роли виртуальной машины без подтверждения</span><span class="sxs-lookup"><span data-stu-id="5f863-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="5f863-124">Первая команда получает облачную службу с именем ContosoVMRole03 с помощью командлета **Get-WAPackVMRole** , а затем сохраняет этот объект в переменной $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5f863-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="5f863-125">Вторая команда удаляет роль виртуальной машины, хранящуюся в $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5f863-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="5f863-126">Эта команда включает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="5f863-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="5f863-127">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5f863-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5f863-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f863-128">PARAMETERS</span></span>

### <span data-ttu-id="5f863-129">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="5f863-129">-CloudServiceName</span></span>
<span data-ttu-id="5f863-130">Указывает имя облачной службы для роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5f863-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f863-131">-Force</span><span class="sxs-lookup"><span data-stu-id="5f863-131">-Force</span></span>
<span data-ttu-id="5f863-132">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5f863-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5f863-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f863-133">-PassThru</span></span>
<span data-ttu-id="5f863-134">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5f863-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5f863-135">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5f863-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5f863-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="5f863-136">-Profile</span></span>
<span data-ttu-id="5f863-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5f863-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f863-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f863-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f863-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="5f863-139">-VMRole</span></span>
<span data-ttu-id="5f863-140">Указывает роль виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5f863-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="5f863-141">Чтобы получить роль виртуальной машины, используйте командлет **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="5f863-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f863-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f863-142">-Confirm</span></span>
<span data-ttu-id="5f863-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5f863-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f863-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f863-144">-WhatIf</span></span>
<span data-ttu-id="5f863-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5f863-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f863-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5f863-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f863-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f863-147">CommonParameters</span></span>
<span data-ttu-id="5f863-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f863-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f863-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f863-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f863-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f863-150">INPUTS</span></span>

## <span data-ttu-id="5f863-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f863-151">OUTPUTS</span></span>

## <span data-ttu-id="5f863-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f863-152">NOTES</span></span>

## <span data-ttu-id="5f863-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f863-153">RELATED LINKS</span></span>

[<span data-ttu-id="5f863-154">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="5f863-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="5f863-155">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="5f863-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="5f863-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="5f863-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


