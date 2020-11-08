---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075504"
---
# <span data-ttu-id="d3c77-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d3c77-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d3c77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3c77-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c77-103">Удаление расширения диагностики Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d3c77-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="d3c77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3c77-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d3c77-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3c77-105">DESCRIPTION</span></span>
<span data-ttu-id="d3c77-106">Командлет **Remove-AzureVMDiagnosticsExtension** удаляет расширение диагностики Microsoft Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d3c77-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="d3c77-107">Выходные данные этого командлета необходимо передать командлету **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="d3c77-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="d3c77-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3c77-108">EXAMPLES</span></span>

### <span data-ttu-id="d3c77-109">Пример 1: удаление расширения диагностики Azure из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d3c77-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="d3c77-110">Эта команда удаляет расширение диагностики Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d3c77-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="d3c77-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3c77-111">PARAMETERS</span></span>

### <span data-ttu-id="d3c77-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d3c77-112">-InformationAction</span></span>
<span data-ttu-id="d3c77-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d3c77-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d3c77-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d3c77-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3c77-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d3c77-115">Continue</span></span>
- <span data-ttu-id="d3c77-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d3c77-116">Ignore</span></span>
- <span data-ttu-id="d3c77-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d3c77-117">Inquire</span></span>
- <span data-ttu-id="d3c77-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d3c77-118">SilentlyContinue</span></span>
- <span data-ttu-id="d3c77-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="d3c77-119">Stop</span></span>
- <span data-ttu-id="d3c77-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="d3c77-120">Suspend</span></span>

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

### <span data-ttu-id="d3c77-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d3c77-121">-InformationVariable</span></span>
<span data-ttu-id="d3c77-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d3c77-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d3c77-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="d3c77-123">-Profile</span></span>
<span data-ttu-id="d3c77-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d3c77-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3c77-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3c77-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3c77-126">-VM</span><span class="sxs-lookup"><span data-stu-id="d3c77-126">-VM</span></span>
<span data-ttu-id="d3c77-127">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d3c77-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="d3c77-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c77-128">CommonParameters</span></span>
<span data-ttu-id="d3c77-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3c77-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c77-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c77-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c77-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3c77-131">INPUTS</span></span>

## <span data-ttu-id="d3c77-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3c77-132">OUTPUTS</span></span>

## <span data-ttu-id="d3c77-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3c77-133">NOTES</span></span>

## <span data-ttu-id="d3c77-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3c77-134">RELATED LINKS</span></span>

[<span data-ttu-id="d3c77-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d3c77-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="d3c77-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d3c77-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="d3c77-137">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d3c77-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


