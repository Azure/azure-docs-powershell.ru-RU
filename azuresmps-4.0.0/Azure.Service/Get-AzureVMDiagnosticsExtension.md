---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E1A3FF-E479-44CD-8147-15408DF3F79A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f8290b0e4f40305495b535b28b2a8f61d7911ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076543"
---
# <span data-ttu-id="21864-101">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="21864-101">Get-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="21864-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21864-102">SYNOPSIS</span></span>
<span data-ttu-id="21864-103">Получает параметры расширения диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="21864-103">Gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="21864-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21864-104">SYNTAX</span></span>

```
Get-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="21864-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21864-105">DESCRIPTION</span></span>
<span data-ttu-id="21864-106">Командлет **Get-AzureVMDiagnosticsExtension** получает параметры расширения диагностики Microsoft Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="21864-106">The **Get-AzureVMDiagnosticsExtension** cmdlet gets the settings of the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="21864-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21864-107">EXAMPLES</span></span>

### <span data-ttu-id="21864-108">Пример 1: получение расширения диагностики, примененного к виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="21864-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVMDiagnosticsExtension -VM $VM
```

<span data-ttu-id="21864-109">Эта команда получает расширение диагностики, примененное к указанной виртуальной машине, в соответствии с переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="21864-109">This command gets the diagnostics extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="21864-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21864-110">PARAMETERS</span></span>

### <span data-ttu-id="21864-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="21864-111">-InformationAction</span></span>
<span data-ttu-id="21864-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="21864-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="21864-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="21864-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21864-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="21864-114">Continue</span></span>
- <span data-ttu-id="21864-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="21864-115">Ignore</span></span>
- <span data-ttu-id="21864-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="21864-116">Inquire</span></span>
- <span data-ttu-id="21864-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="21864-117">SilentlyContinue</span></span>
- <span data-ttu-id="21864-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="21864-118">Stop</span></span>
- <span data-ttu-id="21864-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="21864-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21864-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="21864-120">-InformationVariable</span></span>
<span data-ttu-id="21864-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="21864-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21864-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="21864-122">-Profile</span></span>
<span data-ttu-id="21864-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="21864-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="21864-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="21864-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="21864-125">-VM</span><span class="sxs-lookup"><span data-stu-id="21864-125">-VM</span></span>
<span data-ttu-id="21864-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21864-126">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21864-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21864-127">CommonParameters</span></span>
<span data-ttu-id="21864-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21864-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21864-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21864-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21864-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21864-130">INPUTS</span></span>

## <span data-ttu-id="21864-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21864-131">OUTPUTS</span></span>

## <span data-ttu-id="21864-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="21864-132">NOTES</span></span>

## <span data-ttu-id="21864-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21864-133">RELATED LINKS</span></span>

[<span data-ttu-id="21864-134">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="21864-134">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="21864-135">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="21864-135">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)


