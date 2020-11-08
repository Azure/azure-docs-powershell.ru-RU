---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075531"
---
# <span data-ttu-id="bbe53-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="bbe53-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="bbe53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbe53-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe53-103">Получает сведения из настраиваемого расширения сценария для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe53-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="bbe53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbe53-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bbe53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe53-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe53-106">Командлет **Get-AzureVMCustomScriptExtension** получает сведения из настраиваемого расширения сценария для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe53-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="bbe53-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbe53-107">EXAMPLES</span></span>

### <span data-ttu-id="bbe53-108">Пример 1: получение расширения сценария виртуальной машины Azure</span><span class="sxs-lookup"><span data-stu-id="bbe53-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="bbe53-109">Эта команда получает расширение сценария виртуальной машины Azure, сохраненное в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="bbe53-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="bbe53-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbe53-110">PARAMETERS</span></span>

### <span data-ttu-id="bbe53-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bbe53-111">-InformationAction</span></span>
<span data-ttu-id="bbe53-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="bbe53-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bbe53-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bbe53-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bbe53-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="bbe53-114">Continue</span></span>
- <span data-ttu-id="bbe53-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="bbe53-115">Ignore</span></span>
- <span data-ttu-id="bbe53-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="bbe53-116">Inquire</span></span>
- <span data-ttu-id="bbe53-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bbe53-117">SilentlyContinue</span></span>
- <span data-ttu-id="bbe53-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="bbe53-118">Stop</span></span>
- <span data-ttu-id="bbe53-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="bbe53-119">Suspend</span></span>

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

### <span data-ttu-id="bbe53-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bbe53-120">-InformationVariable</span></span>
<span data-ttu-id="bbe53-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="bbe53-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bbe53-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="bbe53-122">-Profile</span></span>
<span data-ttu-id="bbe53-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bbe53-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bbe53-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbe53-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bbe53-125">-VM</span><span class="sxs-lookup"><span data-stu-id="bbe53-125">-VM</span></span>
<span data-ttu-id="bbe53-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bbe53-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="bbe53-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe53-127">CommonParameters</span></span>
<span data-ttu-id="bbe53-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbe53-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe53-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe53-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe53-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbe53-130">INPUTS</span></span>

## <span data-ttu-id="bbe53-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe53-131">OUTPUTS</span></span>

## <span data-ttu-id="bbe53-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbe53-132">NOTES</span></span>

## <span data-ttu-id="bbe53-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbe53-133">RELATED LINKS</span></span>

[<span data-ttu-id="bbe53-134">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="bbe53-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="bbe53-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="bbe53-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


