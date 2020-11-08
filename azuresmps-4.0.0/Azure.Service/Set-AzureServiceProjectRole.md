---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075952"
---
# <span data-ttu-id="ec040-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="ec040-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="ec040-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec040-102">SYNOPSIS</span></span>
<span data-ttu-id="ec040-103">Задает количество экземпляров или версию среды выполнения роли.</span><span class="sxs-lookup"><span data-stu-id="ec040-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="ec040-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec040-104">SYNTAX</span></span>

### <span data-ttu-id="ec040-105">Образцы</span><span class="sxs-lookup"><span data-stu-id="ec040-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec040-106">Язык</span><span class="sxs-lookup"><span data-stu-id="ec040-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec040-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="ec040-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec040-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec040-108">DESCRIPTION</span></span>
<span data-ttu-id="ec040-109">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ec040-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ec040-110">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ec040-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ec040-111">Командлет **Set-AzureServiceProjectRole** задает количество экземпляров ролей для указанной роли.</span><span class="sxs-lookup"><span data-stu-id="ec040-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="ec040-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec040-112">EXAMPLES</span></span>

### <span data-ttu-id="ec040-113">Пример 1: Настройка экземпляров для веб-роли</span><span class="sxs-lookup"><span data-stu-id="ec040-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="ec040-114">Задает количество экземпляров для веб-роли с именем MyWebRole1 на 2.</span><span class="sxs-lookup"><span data-stu-id="ec040-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="ec040-115">Пример 2: Настройка экземпляров для рабочей роли</span><span class="sxs-lookup"><span data-stu-id="ec040-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="ec040-116">Задает количество экземпляров ролей для роли сотрудника с именем WorkerRole1 на 2.</span><span class="sxs-lookup"><span data-stu-id="ec040-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="ec040-117">Пример 3: Настройка версии среды выполнения для службы роли</span><span class="sxs-lookup"><span data-stu-id="ec040-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="ec040-118">Задает версию среды выполнения node.exe для роли MyRole1 на 0.6.20.</span><span class="sxs-lookup"><span data-stu-id="ec040-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="ec040-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec040-119">PARAMETERS</span></span>

### <span data-ttu-id="ec040-120">-Экземпляры</span><span class="sxs-lookup"><span data-stu-id="ec040-120">-Instances</span></span>
<span data-ttu-id="ec040-121">Задает количество экземпляров ролей для указанной веб-или рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="ec040-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec040-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec040-122">-PassThru</span></span>
<span data-ttu-id="ec040-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ec040-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec040-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ec040-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec040-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="ec040-125">-Profile</span></span>
<span data-ttu-id="ec040-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ec040-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec040-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ec040-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec040-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="ec040-128">-RoleName</span></span>
<span data-ttu-id="ec040-129">Указывает имя изменяемой веб-или рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="ec040-129">Specifies the name of the web or worker role to be changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec040-130">-Runtime</span><span class="sxs-lookup"><span data-stu-id="ec040-130">-Runtime</span></span>
<span data-ttu-id="ec040-131">Задает среду выполнения, которую нужно добавить к указанной роли.</span><span class="sxs-lookup"><span data-stu-id="ec040-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec040-132">-Version</span><span class="sxs-lookup"><span data-stu-id="ec040-132">-Version</span></span>
<span data-ttu-id="ec040-133">Указывает версию среды выполнения, которая должна быть добавлена к роли.</span><span class="sxs-lookup"><span data-stu-id="ec040-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec040-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="ec040-134">-VMSize</span></span>
<span data-ttu-id="ec040-135">Задает размер виртуальной машины для роли.</span><span class="sxs-lookup"><span data-stu-id="ec040-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec040-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec040-136">CommonParameters</span></span>
<span data-ttu-id="ec040-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec040-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec040-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec040-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec040-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec040-139">INPUTS</span></span>

###  
<span data-ttu-id="ec040-140">Задает размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ec040-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="ec040-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec040-141">OUTPUTS</span></span>

## <span data-ttu-id="ec040-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec040-142">NOTES</span></span>

## <span data-ttu-id="ec040-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec040-143">RELATED LINKS</span></span>

[<span data-ttu-id="ec040-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ec040-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


