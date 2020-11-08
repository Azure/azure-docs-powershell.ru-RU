---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075460"
---
# <span data-ttu-id="94359-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="94359-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="94359-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94359-102">SYNOPSIS</span></span>
<span data-ttu-id="94359-103">Упаковывает проект службы в облачный пакет Azure.</span><span class="sxs-lookup"><span data-stu-id="94359-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="94359-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94359-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="94359-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94359-105">DESCRIPTION</span></span>
<span data-ttu-id="94359-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="94359-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="94359-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="94359-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="94359-108">Командлет **Save-AzureServiceProjectPackage** упаковывает проект службы в облачный пакет Azure (\*. cspkg).</span><span class="sxs-lookup"><span data-stu-id="94359-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="94359-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94359-109">EXAMPLES</span></span>

### <span data-ttu-id="94359-110">Пример 1: создание пакета проекта службы</span><span class="sxs-lookup"><span data-stu-id="94359-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="94359-111">В этом примере создается объект \*. cspgk для проекта службы с именем MyAzureServiceProject.</span><span class="sxs-lookup"><span data-stu-id="94359-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="94359-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94359-112">PARAMETERS</span></span>

### <span data-ttu-id="94359-113">-Local</span><span class="sxs-lookup"><span data-stu-id="94359-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94359-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="94359-114">-Profile</span></span>
<span data-ttu-id="94359-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="94359-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="94359-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94359-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="94359-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94359-117">CommonParameters</span></span>
<span data-ttu-id="94359-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94359-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94359-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94359-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94359-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94359-120">INPUTS</span></span>

## <span data-ttu-id="94359-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94359-121">OUTPUTS</span></span>

## <span data-ttu-id="94359-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="94359-122">NOTES</span></span>

## <span data-ttu-id="94359-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94359-123">RELATED LINKS</span></span>

[<span data-ttu-id="94359-124">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="94359-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


