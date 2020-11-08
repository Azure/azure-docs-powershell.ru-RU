---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076389"
---
# <span data-ttu-id="f4e80-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="f4e80-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="f4e80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4e80-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e80-103">Создание необходимых файлов и папок для приложения Node.js, которое будет размещено в облаке с помощью node.exe</span><span class="sxs-lookup"><span data-stu-id="f4e80-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="f4e80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4e80-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4e80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4e80-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e80-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4e80-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f4e80-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f4e80-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f4e80-108">Командлет **Add-AzureNodeWorkerRole** создает необходимые файлы и папки, которые иногда называют механизмом формирования шаблонов, для того чтобы приложение Node.js было размещено в облаке с помощью node.exe.</span><span class="sxs-lookup"><span data-stu-id="f4e80-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="f4e80-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4e80-109">EXAMPLES</span></span>

### <span data-ttu-id="f4e80-110">Пример 1: роль рабочего процесса с одним экземпляром</span><span class="sxs-lookup"><span data-stu-id="f4e80-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="f4e80-111">В этом примере в текущее приложение добавляется формирование шаблонов для одной роли рабочего процесса с именем **MyWorkerRole** .</span><span class="sxs-lookup"><span data-stu-id="f4e80-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="f4e80-112">Пример 2: Рабочая роль для нескольких экземпляров</span><span class="sxs-lookup"><span data-stu-id="f4e80-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="f4e80-113">В этом примере для одной рабочей роли с именем **MyWorkerRole** в текущее приложение добавляется формирование шаблонов с числом экземпляров роли 2.</span><span class="sxs-lookup"><span data-stu-id="f4e80-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="f4e80-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4e80-114">PARAMETERS</span></span>

### <span data-ttu-id="f4e80-115">-Экземпляры</span><span class="sxs-lookup"><span data-stu-id="f4e80-115">-Instances</span></span>
<span data-ttu-id="f4e80-116">Задает количество экземпляров ролей для этой роли рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="f4e80-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="f4e80-117">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="f4e80-117">Default is 1.</span></span>

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

### <span data-ttu-id="f4e80-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4e80-118">-Name</span></span>
<span data-ttu-id="f4e80-119">Указывает имя рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="f4e80-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="f4e80-120">Значение определяет имя папки, содержащей формирование шаблонов для службы node.js, размещенной в рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="f4e80-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="f4e80-121">По умолчанию используется WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="f4e80-121">Default is WorkerRole1.</span></span>

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

### <span data-ttu-id="f4e80-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="f4e80-122">-Profile</span></span>
<span data-ttu-id="f4e80-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f4e80-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4e80-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4e80-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4e80-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e80-125">CommonParameters</span></span>
<span data-ttu-id="f4e80-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4e80-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e80-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e80-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e80-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4e80-128">INPUTS</span></span>

## <span data-ttu-id="f4e80-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4e80-129">OUTPUTS</span></span>

## <span data-ttu-id="f4e80-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4e80-130">NOTES</span></span>

## <span data-ttu-id="f4e80-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4e80-131">RELATED LINKS</span></span>

[<span data-ttu-id="f4e80-132">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="f4e80-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="f4e80-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f4e80-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


