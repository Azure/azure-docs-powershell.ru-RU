---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 501a164fc4470a3d4fd6163050fba495ce3d2705
ms.sourcegitcommit: 25eca7b5f5480758aa2cd830458900cf91cf673c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "95515098"
---
# <span data-ttu-id="e0d2a-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="e0d2a-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="e0d2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d2a-103">Останавливает эмулятор COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="e0d2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0d2a-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0d2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0d2a-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d2a-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e0d2a-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e0d2a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e0d2a-108">Командлет **Stop-AzureEmulator** останавливает эмулятор вычислительной среды Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-108">The **Stop-AzureEmulator** cmdlet stops the Azure Compute Emulator.</span></span>
<span data-ttu-id="e0d2a-109">Все службы, запущенные в данный момент в эмуляторе, удаляются.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="e0d2a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0d2a-110">EXAMPLES</span></span>

## <span data-ttu-id="e0d2a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0d2a-111">PARAMETERS</span></span>

### <span data-ttu-id="e0d2a-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0d2a-112">-PassThru</span></span>
<span data-ttu-id="e0d2a-113">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e0d2a-114">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e0d2a-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e0d2a-115">-Profile</span></span>
<span data-ttu-id="e0d2a-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0d2a-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0d2a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d2a-118">CommonParameters</span></span>
<span data-ttu-id="e0d2a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0d2a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d2a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d2a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d2a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0d2a-121">INPUTS</span></span>

## <span data-ttu-id="e0d2a-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0d2a-122">OUTPUTS</span></span>

## <span data-ttu-id="e0d2a-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0d2a-123">NOTES</span></span>

## <span data-ttu-id="e0d2a-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0d2a-124">RELATED LINKS</span></span>

[<span data-ttu-id="e0d2a-125">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="e0d2a-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


