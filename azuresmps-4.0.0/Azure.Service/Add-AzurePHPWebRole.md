---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076390"
---
# <span data-ttu-id="3dbf5-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="3dbf5-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="3dbf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3dbf5-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbf5-103">Создает необходимые файлы и конфигурацию для приложения PHP.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="3dbf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3dbf5-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3dbf5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dbf5-105">DESCRIPTION</span></span>
<span data-ttu-id="3dbf5-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3dbf5-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3dbf5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3dbf5-108">Командлет **Add-AzurePHPWebRole** создает файлы и конфигурацию, иногда называемые формированием шаблонов, для приложения PHP, которое будет размещено в Azure через IIS.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="3dbf5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3dbf5-109">EXAMPLES</span></span>

### <span data-ttu-id="3dbf5-110">Пример 1: Добавление веб-роли с использованием значений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3dbf5-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="3dbf5-111">В этом примере добавляются необходимые файлы и конфигурация для новой веб-роли с использованием значений по умолчанию для службы с именем "WebRole1" с 1 экземпляром.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="3dbf5-112">Пример 2: Добавление веб-роли с несколькими экземплярами</span><span class="sxs-lookup"><span data-stu-id="3dbf5-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="3dbf5-113">В этом примере в текущее приложение добавляются необходимые файлы и конфигурация для новой веб-роли с именем "MyWebRole", а количество экземпляров роли — 2.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="3dbf5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3dbf5-114">PARAMETERS</span></span>

### <span data-ttu-id="3dbf5-115">-Экземпляры</span><span class="sxs-lookup"><span data-stu-id="3dbf5-115">-Instances</span></span>
<span data-ttu-id="3dbf5-116">Задает количество экземпляров ролей для этой веб-роли.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="3dbf5-117">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-117">The default is 1.</span></span>

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

### <span data-ttu-id="3dbf5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3dbf5-118">-Name</span></span>
<span data-ttu-id="3dbf5-119">Указывает имя веб-роли.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="3dbf5-120">Имя определяет имя каталога, содержащего необходимые файлы и конфигурацию для приложения PHP.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="3dbf5-121">По умолчанию используется значение #, где # — количество веб-ролей в службе.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

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

### <span data-ttu-id="3dbf5-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="3dbf5-122">-Profile</span></span>
<span data-ttu-id="3dbf5-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3dbf5-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3dbf5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbf5-125">CommonParameters</span></span>
<span data-ttu-id="3dbf5-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3dbf5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbf5-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dbf5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbf5-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3dbf5-128">INPUTS</span></span>

## <span data-ttu-id="3dbf5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dbf5-129">OUTPUTS</span></span>

## <span data-ttu-id="3dbf5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3dbf5-130">NOTES</span></span>

## <span data-ttu-id="3dbf5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3dbf5-131">RELATED LINKS</span></span>

[<span data-ttu-id="3dbf5-132">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="3dbf5-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="3dbf5-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="3dbf5-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


