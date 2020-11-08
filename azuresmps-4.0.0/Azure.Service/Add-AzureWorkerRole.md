---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075710"
---
# <span data-ttu-id="cd788-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="cd788-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="cd788-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd788-102">SYNOPSIS</span></span>
<span data-ttu-id="cd788-103">Создает необходимые файлы и конфигурацию для настраиваемой рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="cd788-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="cd788-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd788-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cd788-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd788-105">DESCRIPTION</span></span>
<span data-ttu-id="cd788-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cd788-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cd788-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cd788-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cd788-108">Командлет **Add-AzureWorkerRole** создает необходимые файлы и конфигурацию, иногда называемые формированием шаблонов, для настраиваемой рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="cd788-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="cd788-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd788-109">EXAMPLES</span></span>

### <span data-ttu-id="cd788-110">Пример 1: создание рабочей роли для одного экземпляра</span><span class="sxs-lookup"><span data-stu-id="cd788-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="cd788-111">В этом примере в текущее приложение добавляется формирование шаблонов для одной роли рабочего процесса с именем MyWorkerRole.</span><span class="sxs-lookup"><span data-stu-id="cd788-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="cd788-112">Пример 2: создание рабочей роли для нескольких экземпляров</span><span class="sxs-lookup"><span data-stu-id="cd788-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="cd788-113">Этот пример добавляет формирование шаблонов для новой рабочей роли с именем MyWorkerRole в текущее приложение с количеством экземпляров роли 2.</span><span class="sxs-lookup"><span data-stu-id="cd788-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="cd788-114">Пример 3: Создание роли сотрудника с настраиваемым формированием шаблонов</span><span class="sxs-lookup"><span data-stu-id="cd788-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="cd788-115">В этом примере создается рабочая роль с настраиваемым формированием шаблонов.</span><span class="sxs-lookup"><span data-stu-id="cd788-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="cd788-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd788-116">PARAMETERS</span></span>

### <span data-ttu-id="cd788-117">-Экземпляры</span><span class="sxs-lookup"><span data-stu-id="cd788-117">-Instances</span></span>
<span data-ttu-id="cd788-118">Задает количество экземпляров ролей для этой роли рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="cd788-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="cd788-119">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="cd788-119">The default is 1.</span></span>

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

### <span data-ttu-id="cd788-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd788-120">-Name</span></span>
<span data-ttu-id="cd788-121">Указывает имя рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="cd788-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="cd788-122">Это значение определяет имя папки, содержащей формирование шаблонов для настраиваемого приложения, которое будет размещено в рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="cd788-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="cd788-123">По умолчанию используется WorkerRolenumber, где число — количество рабочих ролей в службе.</span><span class="sxs-lookup"><span data-stu-id="cd788-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

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

### <span data-ttu-id="cd788-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="cd788-124">-Profile</span></span>
<span data-ttu-id="cd788-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cd788-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd788-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cd788-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd788-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="cd788-127">-TemplateFolder</span></span>
<span data-ttu-id="cd788-128">Указывает папку шаблонов формирования шаблонов, которая будет использоваться для создания рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="cd788-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

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

### <span data-ttu-id="cd788-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd788-129">CommonParameters</span></span>
<span data-ttu-id="cd788-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd788-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd788-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd788-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd788-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd788-132">INPUTS</span></span>

## <span data-ttu-id="cd788-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd788-133">OUTPUTS</span></span>

## <span data-ttu-id="cd788-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd788-134">NOTES</span></span>

## <span data-ttu-id="cd788-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd788-135">RELATED LINKS</span></span>

[<span data-ttu-id="cd788-136">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="cd788-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="cd788-137">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="cd788-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


