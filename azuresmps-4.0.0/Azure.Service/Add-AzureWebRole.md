---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075711"
---
# <span data-ttu-id="0f068-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="0f068-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="0f068-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f068-102">SYNOPSIS</span></span>
<span data-ttu-id="0f068-103">Добавление роли веб-рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="0f068-103">Adds a web worker role.</span></span>

## <span data-ttu-id="0f068-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f068-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f068-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f068-105">DESCRIPTION</span></span>
<span data-ttu-id="0f068-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f068-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0f068-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0f068-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0f068-108">Командлет **Add-AzureWebRole** добавляет роль веб-рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="0f068-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="0f068-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f068-109">EXAMPLES</span></span>

### <span data-ttu-id="0f068-110">Пример 1: Добавление роли по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0f068-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="0f068-111">Эта команда добавляет веб-роль с конфигурацией по умолчанию Webrole1 в качестве имени и единственного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0f068-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="0f068-112">Пример 2: Добавление роли с именем</span><span class="sxs-lookup"><span data-stu-id="0f068-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="0f068-113">Эта команда добавляет одну веб-роль с именем MyWebRole в текущее приложение.</span><span class="sxs-lookup"><span data-stu-id="0f068-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="0f068-114">Пример 3: Добавление роли с именем и количеством экземпляров</span><span class="sxs-lookup"><span data-stu-id="0f068-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="0f068-115">Эта команда добавляет в текущее приложение веб-роль с именем MyWebRole.</span><span class="sxs-lookup"><span data-stu-id="0f068-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="0f068-116">Число экземпляров роли в командлете равно 2.</span><span class="sxs-lookup"><span data-stu-id="0f068-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="0f068-117">Пример 4: Добавление роли с именем и шаблоном</span><span class="sxs-lookup"><span data-stu-id="0f068-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="0f068-118">Эта команда добавляет одну веб-роль с именем MyWebRole в текущее приложение.</span><span class="sxs-lookup"><span data-stu-id="0f068-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="0f068-119">Команда задает папку с именем MyWebTemplateFolder в качестве шаблона формирования шаблонов.</span><span class="sxs-lookup"><span data-stu-id="0f068-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="0f068-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f068-120">PARAMETERS</span></span>

### <span data-ttu-id="0f068-121">-Экземпляры</span><span class="sxs-lookup"><span data-stu-id="0f068-121">-Instances</span></span>
<span data-ttu-id="0f068-122">Указывает количество экземпляров.</span><span class="sxs-lookup"><span data-stu-id="0f068-122">Specifies the number of instances.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f068-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f068-123">-Name</span></span>
<span data-ttu-id="0f068-124">Указывает имя веб-роли.</span><span class="sxs-lookup"><span data-stu-id="0f068-124">Specifies the name of the web role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f068-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="0f068-125">-Profile</span></span>
<span data-ttu-id="0f068-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0f068-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f068-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f068-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f068-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="0f068-128">-TemplateFolder</span></span>
<span data-ttu-id="0f068-129">Указывает папку шаблонов.</span><span class="sxs-lookup"><span data-stu-id="0f068-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="0f068-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f068-130">CommonParameters</span></span>
<span data-ttu-id="0f068-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f068-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f068-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f068-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f068-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f068-133">INPUTS</span></span>

## <span data-ttu-id="0f068-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f068-134">OUTPUTS</span></span>

## <span data-ttu-id="0f068-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f068-135">NOTES</span></span>

## <span data-ttu-id="0f068-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f068-136">RELATED LINKS</span></span>

[<span data-ttu-id="0f068-137">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="0f068-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="0f068-138">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="0f068-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


