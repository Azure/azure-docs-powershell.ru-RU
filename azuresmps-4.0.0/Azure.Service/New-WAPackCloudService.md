---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077357"
---
# <span data-ttu-id="d88f5-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="d88f5-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="d88f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d88f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d88f5-103">Создание облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88f5-103">Creates a cloud service.</span></span>

## <span data-ttu-id="d88f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d88f5-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d88f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d88f5-105">DESCRIPTION</span></span>
<span data-ttu-id="d88f5-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="d88f5-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="d88f5-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d88f5-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d88f5-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d88f5-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d88f5-109">Командлет **New-WAPackCloudService** создает облачную службу.</span><span class="sxs-lookup"><span data-stu-id="d88f5-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="d88f5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d88f5-110">EXAMPLES</span></span>

### <span data-ttu-id="d88f5-111">Пример 1: создание облачной службы</span><span class="sxs-lookup"><span data-stu-id="d88f5-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="d88f5-112">Команда создает облачную службу с именем ContosoCloudService01 с меткой.</span><span class="sxs-lookup"><span data-stu-id="d88f5-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="d88f5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d88f5-113">PARAMETERS</span></span>

### <span data-ttu-id="d88f5-114">-Label</span><span class="sxs-lookup"><span data-stu-id="d88f5-114">-Label</span></span>
<span data-ttu-id="d88f5-115">Указывает метку облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88f5-115">Specifies a label for the cloud service.</span></span>

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

### <span data-ttu-id="d88f5-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d88f5-116">-Name</span></span>
<span data-ttu-id="d88f5-117">Задает имя для cloudservice.</span><span class="sxs-lookup"><span data-stu-id="d88f5-117">Specifies a name for the cloudservice.</span></span>

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

### <span data-ttu-id="d88f5-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="d88f5-118">-Profile</span></span>
<span data-ttu-id="d88f5-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d88f5-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d88f5-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d88f5-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d88f5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88f5-121">CommonParameters</span></span>
<span data-ttu-id="d88f5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d88f5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88f5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d88f5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88f5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d88f5-124">INPUTS</span></span>

## <span data-ttu-id="d88f5-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d88f5-125">OUTPUTS</span></span>

## <span data-ttu-id="d88f5-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d88f5-126">NOTES</span></span>

## <span data-ttu-id="d88f5-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d88f5-127">RELATED LINKS</span></span>

[<span data-ttu-id="d88f5-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="d88f5-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="d88f5-129">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="d88f5-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


