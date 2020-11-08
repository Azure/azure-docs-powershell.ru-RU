---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077390"
---
# <span data-ttu-id="e5333-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="e5333-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="e5333-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5333-102">SYNOPSIS</span></span>
<span data-ttu-id="e5333-103">Создание роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5333-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="e5333-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5333-104">SYNTAX</span></span>

### <span data-ttu-id="e5333-105">QuickCreate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5333-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e5333-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="e5333-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e5333-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5333-107">DESCRIPTION</span></span>
<span data-ttu-id="e5333-108">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="e5333-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e5333-109">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5333-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e5333-110">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e5333-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e5333-111">Командлет **New-WAPackVMRole** создает роль виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5333-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="e5333-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5333-112">EXAMPLES</span></span>

### <span data-ttu-id="e5333-113">Пример 1: Создание роли виртуальной машины (эмуляция поведения WAP)</span><span class="sxs-lookup"><span data-stu-id="e5333-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="e5333-114">Так как мы не указываем облачные службы (эмуляция поведения WAP), команда создаст облачную службу для US, имя которой будет совпадать с именем роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5333-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="e5333-115">В этом случае следующая команда создаст роль виртуальной машины с именем ContosoVMRole01, меткой ContosoVMRoleLabel01.</span><span class="sxs-lookup"><span data-stu-id="e5333-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="e5333-116">Обратите внимание, что описанное здесь определение ресурса должно быть создано вручную несмотря на то, что вы используете PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5333-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="e5333-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5333-117">PARAMETERS</span></span>

### <span data-ttu-id="e5333-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="e5333-118">-CloudService</span></span>
<span data-ttu-id="e5333-119">Указывает облачную службу для роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5333-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5333-120">-Label</span><span class="sxs-lookup"><span data-stu-id="e5333-120">-Label</span></span>
<span data-ttu-id="e5333-121">Указывает метку для роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5333-121">Specifies a label for the virtual machine role.</span></span>

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

### <span data-ttu-id="e5333-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5333-122">-Name</span></span>
<span data-ttu-id="e5333-123">Указывает имя для роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5333-123">Specifies a name for the virtual machine role.</span></span>

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

### <span data-ttu-id="e5333-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="e5333-124">-Profile</span></span>
<span data-ttu-id="e5333-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e5333-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5333-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5333-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5333-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="e5333-127">-ResourceDefinition</span></span>
<span data-ttu-id="e5333-128">Указывает определение ресурса для роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5333-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5333-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5333-129">CommonParameters</span></span>
<span data-ttu-id="e5333-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5333-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5333-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5333-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5333-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5333-132">INPUTS</span></span>

## <span data-ttu-id="e5333-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5333-133">OUTPUTS</span></span>

## <span data-ttu-id="e5333-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5333-134">NOTES</span></span>

## <span data-ttu-id="e5333-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5333-135">RELATED LINKS</span></span>

[<span data-ttu-id="e5333-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="e5333-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="e5333-137">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="e5333-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="e5333-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="e5333-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


