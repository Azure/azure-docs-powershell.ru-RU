---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077400"
---
# <span data-ttu-id="a1253-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="a1253-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="a1253-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1253-102">SYNOPSIS</span></span>
<span data-ttu-id="a1253-103">Создание виртуальной машины на основе шаблона.</span><span class="sxs-lookup"><span data-stu-id="a1253-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="a1253-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1253-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a1253-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1253-105">DESCRIPTION</span></span>
<span data-ttu-id="a1253-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="a1253-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="a1253-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a1253-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a1253-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a1253-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a1253-109">Командлет **New-WAPackQuickVM** создает виртуальную машину на основе шаблона.</span><span class="sxs-lookup"><span data-stu-id="a1253-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="a1253-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1253-110">EXAMPLES</span></span>

### <span data-ttu-id="a1253-111">Пример 1: создание виртуальной машины на основе шаблона</span><span class="sxs-lookup"><span data-stu-id="a1253-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="a1253-112">Для первой команды создается объект **PSCredential** , который затем сохраняется в переменной $Credentials.</span><span class="sxs-lookup"><span data-stu-id="a1253-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="a1253-113">Командлет запрашивает учетные записи и пароль.</span><span class="sxs-lookup"><span data-stu-id="a1253-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="a1253-114">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a1253-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="a1253-115">Вторая команда получает шаблон с помощью командлета **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="a1253-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="a1253-116">Команда задает идентификатор шаблона.</span><span class="sxs-lookup"><span data-stu-id="a1253-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="a1253-117">Команда сохраняет объект шаблона в переменной $TemplateID.</span><span class="sxs-lookup"><span data-stu-id="a1253-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="a1253-118">Последняя команда создает виртуальную машину с именем VirtualMachine023.</span><span class="sxs-lookup"><span data-stu-id="a1253-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="a1253-119">Команда помещает виртуальную машину в шаблон, хранящийся в $TemplateId.</span><span class="sxs-lookup"><span data-stu-id="a1253-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="a1253-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1253-120">PARAMETERS</span></span>

### <span data-ttu-id="a1253-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1253-121">-Name</span></span>
<span data-ttu-id="a1253-122">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a1253-122">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="a1253-123">-Profile</span></span>
<span data-ttu-id="a1253-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a1253-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1253-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1253-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1253-126">-Template</span><span class="sxs-lookup"><span data-stu-id="a1253-126">-Template</span></span>
<span data-ttu-id="a1253-127">Задает шаблон.</span><span class="sxs-lookup"><span data-stu-id="a1253-127">Specifies a template.</span></span>
<span data-ttu-id="a1253-128">Командлет создает виртуальную машину на основе указанного шаблона.</span><span class="sxs-lookup"><span data-stu-id="a1253-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="a1253-129">Чтобы получить объект шаблона, используйте командлет **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="a1253-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="a1253-130">-VMCredential</span></span>
<span data-ttu-id="a1253-131">Задает учетные данные для учетной записи локального администратора.</span><span class="sxs-lookup"><span data-stu-id="a1253-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="a1253-132">Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="a1253-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="a1253-133">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a1253-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1253-134">CommonParameters</span></span>
<span data-ttu-id="a1253-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1253-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1253-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1253-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1253-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1253-137">INPUTS</span></span>

## <span data-ttu-id="a1253-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1253-138">OUTPUTS</span></span>

## <span data-ttu-id="a1253-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1253-139">NOTES</span></span>

## <span data-ttu-id="a1253-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1253-140">RELATED LINKS</span></span>

[<span data-ttu-id="a1253-141">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a1253-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="a1253-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="a1253-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


