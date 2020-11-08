---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076448"
---
# <span data-ttu-id="57e81-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="57e81-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="57e81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57e81-102">SYNOPSIS</span></span>
<span data-ttu-id="57e81-103">Удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="57e81-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="57e81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57e81-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="57e81-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57e81-105">DESCRIPTION</span></span>
<span data-ttu-id="57e81-106">Командлет **Remove-AzureVMCustomScriptExtension** Удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="57e81-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="57e81-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57e81-107">EXAMPLES</span></span>

### <span data-ttu-id="57e81-108">Пример 1: удаление расширения настраиваемого сценария для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="57e81-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="57e81-109">Эта команда удаляет расширение настраиваемого сценария виртуальной машины Azure из указанной виртуальной машины, как оно хранится в $VM переменной.</span><span class="sxs-lookup"><span data-stu-id="57e81-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="57e81-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57e81-110">PARAMETERS</span></span>

### <span data-ttu-id="57e81-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="57e81-111">-InformationAction</span></span>
<span data-ttu-id="57e81-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="57e81-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="57e81-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="57e81-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57e81-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="57e81-114">Continue</span></span>
- <span data-ttu-id="57e81-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="57e81-115">Ignore</span></span>
- <span data-ttu-id="57e81-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="57e81-116">Inquire</span></span>
- <span data-ttu-id="57e81-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="57e81-117">SilentlyContinue</span></span>
- <span data-ttu-id="57e81-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="57e81-118">Stop</span></span>
- <span data-ttu-id="57e81-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="57e81-119">Suspend</span></span>

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

### <span data-ttu-id="57e81-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="57e81-120">-InformationVariable</span></span>
<span data-ttu-id="57e81-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="57e81-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="57e81-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="57e81-122">-Profile</span></span>
<span data-ttu-id="57e81-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="57e81-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57e81-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57e81-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57e81-125">-VM</span><span class="sxs-lookup"><span data-stu-id="57e81-125">-VM</span></span>
<span data-ttu-id="57e81-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="57e81-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="57e81-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e81-127">CommonParameters</span></span>
<span data-ttu-id="57e81-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57e81-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e81-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e81-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e81-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57e81-130">INPUTS</span></span>

## <span data-ttu-id="57e81-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57e81-131">OUTPUTS</span></span>

## <span data-ttu-id="57e81-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="57e81-132">NOTES</span></span>

## <span data-ttu-id="57e81-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57e81-133">RELATED LINKS</span></span>

[<span data-ttu-id="57e81-134">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="57e81-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="57e81-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="57e81-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


