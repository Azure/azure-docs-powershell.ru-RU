---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076031"
---
# <span data-ttu-id="d1df4-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="d1df4-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="d1df4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1df4-102">SYNOPSIS</span></span>
<span data-ttu-id="d1df4-103">Запускает Эмуляторы COMPUTE и Storage.</span><span class="sxs-lookup"><span data-stu-id="d1df4-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="d1df4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1df4-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d1df4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1df4-105">DESCRIPTION</span></span>
<span data-ttu-id="d1df4-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d1df4-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d1df4-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d1df4-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d1df4-108">Командлет **Start-AzureEmulator** запускает обе Эмуляторы COMPUTE и Storage и размещает текущую службу в эмуляторе вычислений.</span><span class="sxs-lookup"><span data-stu-id="d1df4-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="d1df4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1df4-109">EXAMPLES</span></span>

### <span data-ttu-id="d1df4-110">Пример 1: Запуск эмулятора и запуск браузера</span><span class="sxs-lookup"><span data-stu-id="d1df4-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="d1df4-111">В этом примере служба запускается в эмуляторе Azure и запускается новое окно браузера в эмулируемой службе.</span><span class="sxs-lookup"><span data-stu-id="d1df4-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="d1df4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1df4-112">PARAMETERS</span></span>

### <span data-ttu-id="d1df4-113">-Launch</span><span class="sxs-lookup"><span data-stu-id="d1df4-113">-Launch</span></span>
<span data-ttu-id="d1df4-114">Открытие нового окна браузера в службе после ее размещения в эмуляторе.</span><span class="sxs-lookup"><span data-stu-id="d1df4-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1df4-115">Режим</span><span class="sxs-lookup"><span data-stu-id="d1df4-115">-Mode</span></span>
<span data-ttu-id="d1df4-116">Задает режим эмулятора.</span><span class="sxs-lookup"><span data-stu-id="d1df4-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="d1df4-117">Допустимые значения: Full и Express.</span><span class="sxs-lookup"><span data-stu-id="d1df4-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="d1df4-118">Значение по умолчанию — Express.</span><span class="sxs-lookup"><span data-stu-id="d1df4-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1df4-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="d1df4-119">-Profile</span></span>
<span data-ttu-id="d1df4-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d1df4-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1df4-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d1df4-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d1df4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1df4-122">CommonParameters</span></span>
<span data-ttu-id="d1df4-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1df4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1df4-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1df4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1df4-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1df4-125">INPUTS</span></span>

## <span data-ttu-id="d1df4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1df4-126">OUTPUTS</span></span>

## <span data-ttu-id="d1df4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1df4-127">NOTES</span></span>

## <span data-ttu-id="d1df4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1df4-128">RELATED LINKS</span></span>

[<span data-ttu-id="d1df4-129">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d1df4-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="d1df4-130">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d1df4-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="d1df4-131">Остановить-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="d1df4-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


