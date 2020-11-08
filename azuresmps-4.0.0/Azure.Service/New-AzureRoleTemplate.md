---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075992"
---
# <span data-ttu-id="a1531-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="a1531-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="a1531-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1531-102">SYNOPSIS</span></span>
<span data-ttu-id="a1531-103">Создает шаблоны веб-и рабочих ролей.</span><span class="sxs-lookup"><span data-stu-id="a1531-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="a1531-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1531-104">SYNTAX</span></span>

### <span data-ttu-id="a1531-105">Роль "Администратор"</span><span class="sxs-lookup"><span data-stu-id="a1531-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a1531-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="a1531-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a1531-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1531-107">DESCRIPTION</span></span>
<span data-ttu-id="a1531-108">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a1531-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a1531-109">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a1531-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a1531-110">Командлет **New-AzureRoleTemplate** создает шаблоны веб-роли и рабочих ролей.</span><span class="sxs-lookup"><span data-stu-id="a1531-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="a1531-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1531-111">EXAMPLES</span></span>

### <span data-ttu-id="a1531-112">Пример 1: Создание шаблона веб-роли</span><span class="sxs-lookup"><span data-stu-id="a1531-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="a1531-113">В этом примере создается новый шаблон веб-роли в папке с именем WebRoleTemplate в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a1531-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="a1531-114">Пример 2: Создание шаблона рабочей роли</span><span class="sxs-lookup"><span data-stu-id="a1531-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="a1531-115">В этом примере создается новый шаблон рабочей роли в папке с именем WebRoleTemplate в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a1531-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="a1531-116">Пример 3: Создание шаблона роли в настраиваемом каталоге</span><span class="sxs-lookup"><span data-stu-id="a1531-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="a1531-117">В этом примере создается новый шаблон веб-роли в каталоге с именем MyWebRoleTemplate, а не в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a1531-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="a1531-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1531-118">PARAMETERS</span></span>

### <span data-ttu-id="a1531-119">-Output</span><span class="sxs-lookup"><span data-stu-id="a1531-119">-Output</span></span>
<span data-ttu-id="a1531-120">Указывает путь вывода для созданного шаблона.</span><span class="sxs-lookup"><span data-stu-id="a1531-120">Specifies the output path of generated template.</span></span>

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

### <span data-ttu-id="a1531-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="a1531-121">-Profile</span></span>
<span data-ttu-id="a1531-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a1531-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1531-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1531-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1531-124">-Веб-сайт</span><span class="sxs-lookup"><span data-stu-id="a1531-124">-Web</span></span>
<span data-ttu-id="a1531-125">Указывает, что вы хотите создать шаблон веб-роли.</span><span class="sxs-lookup"><span data-stu-id="a1531-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1531-126">-Исполнитель</span><span class="sxs-lookup"><span data-stu-id="a1531-126">-Worker</span></span>
<span data-ttu-id="a1531-127">Указывает, что вы хотите создать шаблон роли рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="a1531-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1531-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1531-128">CommonParameters</span></span>
<span data-ttu-id="a1531-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1531-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1531-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1531-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1531-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1531-131">INPUTS</span></span>

## <span data-ttu-id="a1531-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1531-132">OUTPUTS</span></span>

## <span data-ttu-id="a1531-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1531-133">NOTES</span></span>

## <span data-ttu-id="a1531-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1531-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1531-135">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="a1531-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="a1531-136">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="a1531-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


