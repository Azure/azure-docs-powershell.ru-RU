---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 93A8B8EC-4ED0-4C87-AF92-9A246ECEF4F0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1b516722b0555c84400c0c8f5acd7f1b5c43d9c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075510"
---
# <span data-ttu-id="a915b-101">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a915b-101">Remove-AzureVMAccessExtension</span></span>

## <span data-ttu-id="a915b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a915b-102">SYNOPSIS</span></span>
<span data-ttu-id="a915b-103">Удаляет расширение VMAccess, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a915b-103">Removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a915b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a915b-104">SYNTAX</span></span>

```
Remove-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a915b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a915b-105">DESCRIPTION</span></span>
<span data-ttu-id="a915b-106">Командлет **Remove-AzureVMAccessExtension** удаляет расширение VMAccess, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a915b-106">The **Remove-AzureVMAccessExtension** cmdlet removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a915b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a915b-107">EXAMPLES</span></span>

### <span data-ttu-id="a915b-108">Пример 1: удаление расширения VMAccess из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="a915b-108">Example 1: Remove a VMAccess extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="a915b-109">Эта команда удаляет расширение VMAccess из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a915b-109">This command removes a VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="a915b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a915b-110">PARAMETERS</span></span>

### <span data-ttu-id="a915b-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a915b-111">-InformationAction</span></span>
<span data-ttu-id="a915b-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a915b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a915b-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a915b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a915b-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a915b-114">Continue</span></span>
- <span data-ttu-id="a915b-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a915b-115">Ignore</span></span>
- <span data-ttu-id="a915b-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a915b-116">Inquire</span></span>
- <span data-ttu-id="a915b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a915b-117">SilentlyContinue</span></span>
- <span data-ttu-id="a915b-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="a915b-118">Stop</span></span>
- <span data-ttu-id="a915b-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="a915b-119">Suspend</span></span>

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

### <span data-ttu-id="a915b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a915b-120">-InformationVariable</span></span>
<span data-ttu-id="a915b-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a915b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a915b-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="a915b-122">-Profile</span></span>
<span data-ttu-id="a915b-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a915b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a915b-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a915b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a915b-125">-VM</span><span class="sxs-lookup"><span data-stu-id="a915b-125">-VM</span></span>
<span data-ttu-id="a915b-126">Указывает Сохраняемый объект виртуальной машины, из которого этот командлет удаляет расширение VMAccess.</span><span class="sxs-lookup"><span data-stu-id="a915b-126">Specifies the persistent virtual machine object that this cmdlet removes the VMAccess extension from.</span></span>

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

### <span data-ttu-id="a915b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a915b-127">CommonParameters</span></span>
<span data-ttu-id="a915b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a915b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a915b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a915b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a915b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a915b-130">INPUTS</span></span>

## <span data-ttu-id="a915b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a915b-131">OUTPUTS</span></span>

## <span data-ttu-id="a915b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a915b-132">NOTES</span></span>

## <span data-ttu-id="a915b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a915b-133">RELATED LINKS</span></span>

[<span data-ttu-id="a915b-134">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a915b-134">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="a915b-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a915b-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


