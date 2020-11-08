---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075535"
---
# <span data-ttu-id="14743-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="14743-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="14743-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14743-102">SYNOPSIS</span></span>
<span data-ttu-id="14743-103">Получает расширение VMAccess, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="14743-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="14743-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14743-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="14743-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14743-105">DESCRIPTION</span></span>
<span data-ttu-id="14743-106">Командлет **Get-AzureVMAccessExtension** получает расширение VMAccess, примененное на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="14743-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="14743-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14743-107">EXAMPLES</span></span>

### <span data-ttu-id="14743-108">Пример 1: получение расширения VMAccess для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="14743-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="14743-109">Эта команда получает расширение VMAccess для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="14743-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="14743-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14743-110">PARAMETERS</span></span>

### <span data-ttu-id="14743-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="14743-111">-InformationAction</span></span>
<span data-ttu-id="14743-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="14743-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="14743-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="14743-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="14743-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="14743-114">Continue</span></span>
- <span data-ttu-id="14743-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="14743-115">Ignore</span></span>
- <span data-ttu-id="14743-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="14743-116">Inquire</span></span>
- <span data-ttu-id="14743-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="14743-117">SilentlyContinue</span></span>
- <span data-ttu-id="14743-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="14743-118">Stop</span></span>
- <span data-ttu-id="14743-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="14743-119">Suspend</span></span>

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

### <span data-ttu-id="14743-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="14743-120">-InformationVariable</span></span>
<span data-ttu-id="14743-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="14743-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="14743-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="14743-122">-Profile</span></span>
<span data-ttu-id="14743-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="14743-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14743-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14743-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14743-125">-VM</span><span class="sxs-lookup"><span data-stu-id="14743-125">-VM</span></span>
<span data-ttu-id="14743-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="14743-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="14743-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14743-127">CommonParameters</span></span>
<span data-ttu-id="14743-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14743-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14743-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14743-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14743-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14743-130">INPUTS</span></span>

## <span data-ttu-id="14743-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14743-131">OUTPUTS</span></span>

## <span data-ttu-id="14743-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="14743-132">NOTES</span></span>

## <span data-ttu-id="14743-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14743-133">RELATED LINKS</span></span>

[<span data-ttu-id="14743-134">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="14743-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="14743-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="14743-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


