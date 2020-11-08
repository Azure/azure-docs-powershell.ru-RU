---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075807"
---
# <span data-ttu-id="f2bee-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="f2bee-101">Stop-AzureService</span></span>

## <span data-ttu-id="f2bee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2bee-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bee-103">Останавливает текущую размещенную службу.</span><span class="sxs-lookup"><span data-stu-id="f2bee-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="f2bee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2bee-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2bee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2bee-105">DESCRIPTION</span></span>
<span data-ttu-id="f2bee-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f2bee-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f2bee-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f2bee-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f2bee-108">Командлет **Stop-AzureService** останавливает текущую размещенную службу в указанном слоте в Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bee-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="f2bee-109">Если ячейка не указана, командлет останавливает службу в производственном слоте.</span><span class="sxs-lookup"><span data-stu-id="f2bee-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="f2bee-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2bee-110">EXAMPLES</span></span>

## <span data-ttu-id="f2bee-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2bee-111">PARAMETERS</span></span>

### <span data-ttu-id="f2bee-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2bee-112">-PassThru</span></span>
<span data-ttu-id="f2bee-113">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f2bee-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f2bee-114">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f2bee-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2bee-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="f2bee-115">-Profile</span></span>
<span data-ttu-id="f2bee-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f2bee-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2bee-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2bee-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2bee-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f2bee-118">-ServiceName</span></span>
<span data-ttu-id="f2bee-119">Указывает имя размещенной службы, которую нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="f2bee-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="f2bee-120">Если имя не задано, командлет останавливает текущую размещенную службу.</span><span class="sxs-lookup"><span data-stu-id="f2bee-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="f2bee-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="f2bee-121">-Slot</span></span>
<span data-ttu-id="f2bee-122">Указывает область, в которой размещена служба, как промежуточный или производственный.</span><span class="sxs-lookup"><span data-stu-id="f2bee-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="f2bee-123">Если ячейка не указана, предполагается производство.</span><span class="sxs-lookup"><span data-stu-id="f2bee-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="f2bee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bee-124">CommonParameters</span></span>
<span data-ttu-id="f2bee-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2bee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bee-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2bee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bee-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2bee-127">INPUTS</span></span>

## <span data-ttu-id="f2bee-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2bee-128">OUTPUTS</span></span>

## <span data-ttu-id="f2bee-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2bee-129">NOTES</span></span>

## <span data-ttu-id="f2bee-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2bee-130">RELATED LINKS</span></span>

[<span data-ttu-id="f2bee-131">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="f2bee-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="f2bee-132">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="f2bee-132">Start-AzureService</span></span>](./Start-AzureService.md)


