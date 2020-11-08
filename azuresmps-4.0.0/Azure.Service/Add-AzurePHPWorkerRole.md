---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076387"
---
# <span data-ttu-id="0d122-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="0d122-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="0d122-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d122-102">SYNOPSIS</span></span>
<span data-ttu-id="0d122-103">Создает необходимые файлы и конфигурацию для приложения PHP, которое будет размещено в Azure с помощью php.exe.</span><span class="sxs-lookup"><span data-stu-id="0d122-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="0d122-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d122-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d122-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d122-105">DESCRIPTION</span></span>
<span data-ttu-id="0d122-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d122-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0d122-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0d122-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0d122-108">Создает необходимые файлы и конфигурацию, иногда называемые формированием шаблонов, для приложения PHP, которое будет размещено в Azure с помощью php.exe.</span><span class="sxs-lookup"><span data-stu-id="0d122-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="0d122-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d122-109">EXAMPLES</span></span>

### <span data-ttu-id="0d122-110">Пример 1: создание рабочей роли с одним экземпляром</span><span class="sxs-lookup"><span data-stu-id="0d122-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="0d122-111">В этом примере в текущее приложение добавляются необходимые файлы и конфигурация для одной роли рабочего процесса с именем MyWorkerRole.</span><span class="sxs-lookup"><span data-stu-id="0d122-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="0d122-112">Пример 2: Создание роли рабочего процесса с несколькими экземплярами</span><span class="sxs-lookup"><span data-stu-id="0d122-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="0d122-113">В этом примере в текущее приложение добавляются необходимые файлы и параметры для новой рабочей роли, используя имя MyWorkerRole с числом экземпляров роли 2.</span><span class="sxs-lookup"><span data-stu-id="0d122-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="0d122-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d122-114">PARAMETERS</span></span>

### <span data-ttu-id="0d122-115">-Экземпляры</span><span class="sxs-lookup"><span data-stu-id="0d122-115">-Instances</span></span>
<span data-ttu-id="0d122-116">Задает количество экземпляров ролей для этой роли рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="0d122-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="0d122-117">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="0d122-117">The default is 1.</span></span>

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

### <span data-ttu-id="0d122-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d122-118">-Name</span></span>
<span data-ttu-id="0d122-119">Указывает имя рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="0d122-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="0d122-120">Имя определяет имя папки, которая включает необходимые файлы и конфигурацию для службы PHP, размещенной в рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="0d122-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="0d122-121">Значение по умолчанию — WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="0d122-121">The default is WorkerRole1.</span></span>

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

### <span data-ttu-id="0d122-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="0d122-122">-Profile</span></span>
<span data-ttu-id="0d122-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d122-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d122-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d122-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d122-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d122-125">CommonParameters</span></span>
<span data-ttu-id="0d122-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d122-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d122-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d122-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d122-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d122-128">INPUTS</span></span>

## <span data-ttu-id="0d122-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d122-129">OUTPUTS</span></span>

## <span data-ttu-id="0d122-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d122-130">NOTES</span></span>

## <span data-ttu-id="0d122-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d122-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d122-132">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="0d122-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="0d122-133">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="0d122-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


