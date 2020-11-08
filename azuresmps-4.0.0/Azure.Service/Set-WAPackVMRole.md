---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077383"
---
# <span data-ttu-id="69cb3-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="69cb3-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="69cb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="69cb3-103">Изменяет свойство Count экземпляров роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="69cb3-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="69cb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69cb3-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="69cb3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="69cb3-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="69cb3-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="69cb3-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="69cb3-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="69cb3-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="69cb3-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="69cb3-109">Командлет **Set-WAPackVMRole** изменяет свойство Count экземпляров роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="69cb3-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="69cb3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69cb3-110">EXAMPLES</span></span>

### <span data-ttu-id="69cb3-111">Пример 1: указание количества экземпляров для роли виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="69cb3-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="69cb3-112">Первая команда получает роль виртуальной машины с именем ContosoVMRole01 с помощью командлета **Get-WAPackVMRole** , а затем сохраняет этот объект в переменной $VMRole.</span><span class="sxs-lookup"><span data-stu-id="69cb3-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="69cb3-113">Вторая и последняя команды задают новое количество экземпляров роли виртуальной машины, сохраненной в $VMRole, в 3.</span><span class="sxs-lookup"><span data-stu-id="69cb3-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="69cb3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69cb3-114">PARAMETERS</span></span>

### <span data-ttu-id="69cb3-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="69cb3-115">-InstanceCount</span></span>
<span data-ttu-id="69cb3-116">Задает количество экземпляров роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="69cb3-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69cb3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69cb3-117">-PassThru</span></span>
<span data-ttu-id="69cb3-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="69cb3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69cb3-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="69cb3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69cb3-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="69cb3-120">-Profile</span></span>
<span data-ttu-id="69cb3-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69cb3-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69cb3-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69cb3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69cb3-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="69cb3-123">-VMRole</span></span>
<span data-ttu-id="69cb3-124">Указывает роль виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="69cb3-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="69cb3-125">Чтобы получить роль виртуальной машины, используйте командлет **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="69cb3-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

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

### <span data-ttu-id="69cb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69cb3-126">CommonParameters</span></span>
<span data-ttu-id="69cb3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69cb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69cb3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69cb3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69cb3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69cb3-129">INPUTS</span></span>

## <span data-ttu-id="69cb3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69cb3-130">OUTPUTS</span></span>

## <span data-ttu-id="69cb3-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="69cb3-131">NOTES</span></span>

## <span data-ttu-id="69cb3-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69cb3-132">RELATED LINKS</span></span>

[<span data-ttu-id="69cb3-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="69cb3-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="69cb3-134">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="69cb3-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="69cb3-135">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="69cb3-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


