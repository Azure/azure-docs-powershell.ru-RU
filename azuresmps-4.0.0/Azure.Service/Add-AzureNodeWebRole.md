---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076392"
---
# <span data-ttu-id="2251e-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="2251e-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="2251e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2251e-102">SYNOPSIS</span></span>
<span data-ttu-id="2251e-103">Создание необходимых файлов и папок для приложения Node.js.</span><span class="sxs-lookup"><span data-stu-id="2251e-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="2251e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2251e-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2251e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2251e-105">DESCRIPTION</span></span>
<span data-ttu-id="2251e-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2251e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2251e-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2251e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2251e-108">**Надстройка Add-AzureNodeWebRole** создает необходимые файлы и папки, которые иногда называют обоснованными, для того чтобы приложение Node.js было размещено в облаке через IIS.</span><span class="sxs-lookup"><span data-stu-id="2251e-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="2251e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2251e-109">EXAMPLES</span></span>

### <span data-ttu-id="2251e-110">Пример 1: веб-роль «один экземпляр»</span><span class="sxs-lookup"><span data-stu-id="2251e-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="2251e-111">В этом примере в текущее приложение добавляется формирование шаблонов для одной веб-роли с именем **MyWebRole** .</span><span class="sxs-lookup"><span data-stu-id="2251e-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="2251e-112">Пример 2: веб-роль для нескольких экземпляров</span><span class="sxs-lookup"><span data-stu-id="2251e-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="2251e-113">В этом примере добавляется формирование шаблонов для новой веб-роли с именем **MyWebRole** в текущее приложение с количеством экземпляров роли 2.</span><span class="sxs-lookup"><span data-stu-id="2251e-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="2251e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2251e-114">PARAMETERS</span></span>

### <span data-ttu-id="2251e-115">-Экземпляры</span><span class="sxs-lookup"><span data-stu-id="2251e-115">-Instances</span></span>
<span data-ttu-id="2251e-116">Задает количество экземпляров ролей для этой веб-роли.</span><span class="sxs-lookup"><span data-stu-id="2251e-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="2251e-117">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="2251e-117">The default is 1.</span></span>

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

### <span data-ttu-id="2251e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2251e-118">-Name</span></span>
<span data-ttu-id="2251e-119">Указывает имя веб-роли.</span><span class="sxs-lookup"><span data-stu-id="2251e-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="2251e-120">Кроме того, он определяет имя каталога, содержащего формирование шаблонов для приложения node.js, которое будет размещаться в веб-роли.</span><span class="sxs-lookup"><span data-stu-id="2251e-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="2251e-121">По умолчанию используется значение #, где # указывает количество веб-ролей в службе.</span><span class="sxs-lookup"><span data-stu-id="2251e-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="2251e-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="2251e-122">-Profile</span></span>
<span data-ttu-id="2251e-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2251e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2251e-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2251e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2251e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2251e-125">CommonParameters</span></span>
<span data-ttu-id="2251e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2251e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2251e-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2251e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2251e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2251e-128">INPUTS</span></span>

## <span data-ttu-id="2251e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2251e-129">OUTPUTS</span></span>

## <span data-ttu-id="2251e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2251e-130">NOTES</span></span>

## <span data-ttu-id="2251e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2251e-131">RELATED LINKS</span></span>

[<span data-ttu-id="2251e-132">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="2251e-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="2251e-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2251e-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


