---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076218"
---
# <span data-ttu-id="db829-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="db829-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="db829-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db829-102">SYNOPSIS</span></span>
<span data-ttu-id="db829-103">Создание необходимых файлов и конфигурации для новой службы.</span><span class="sxs-lookup"><span data-stu-id="db829-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="db829-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db829-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db829-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db829-105">DESCRIPTION</span></span>
<span data-ttu-id="db829-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="db829-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="db829-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="db829-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="db829-108">Командлет **New-AzureServiceProject** создает необходимые файлы и конфигурацию для новой службы Azure в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="db829-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="db829-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db829-109">EXAMPLES</span></span>

### <span data-ttu-id="db829-110">Пример 1: создание формирования шаблонов для службы</span><span class="sxs-lookup"><span data-stu-id="db829-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="db829-111">В этом примере создается формирование шаблонов для новой службы Azure с именем MyService1 в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="db829-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="db829-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db829-112">PARAMETERS</span></span>

### <span data-ttu-id="db829-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="db829-113">-Profile</span></span>
<span data-ttu-id="db829-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="db829-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db829-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db829-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db829-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="db829-116">-ServiceName</span></span>
<span data-ttu-id="db829-117">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="db829-117">Specifies the name of the service.</span></span>
<span data-ttu-id="db829-118">Он определяет первый раздел имени узла для службы (например, name.cloudapp.net), а также каталог, который будет содержать службу.</span><span class="sxs-lookup"><span data-stu-id="db829-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="db829-119">Имя может содержать только буквы, цифры и знаки тире (-).</span><span class="sxs-lookup"><span data-stu-id="db829-119">The name can contain only letters, digits, and the dash character (-).</span></span>

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

### <span data-ttu-id="db829-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db829-120">CommonParameters</span></span>
<span data-ttu-id="db829-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db829-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db829-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db829-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db829-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db829-123">INPUTS</span></span>

## <span data-ttu-id="db829-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db829-124">OUTPUTS</span></span>

## <span data-ttu-id="db829-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="db829-125">NOTES</span></span>

## <span data-ttu-id="db829-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db829-126">RELATED LINKS</span></span>

[<span data-ttu-id="db829-127">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="db829-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="db829-128">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="db829-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="db829-129">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="db829-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="db829-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="db829-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="db829-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="db829-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


