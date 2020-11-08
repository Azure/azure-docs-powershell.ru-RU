---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075673"
---
# <span data-ttu-id="43ef9-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="43ef9-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="43ef9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="43ef9-103">Получает объект конфигурации ACL из виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="43ef9-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="43ef9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43ef9-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="43ef9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="43ef9-106">Командлет **Get-AzureAclConfig** получает объект конфигурации списка управления доступом (ACL) с существующей виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="43ef9-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="43ef9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="43ef9-108">Пример 1: получение объекта конфигурации ACL для конечной точки виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="43ef9-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="43ef9-109">Первая команда получает виртуальную машину с именем VirtualMachine07 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="43ef9-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="43ef9-110">Команда передает этот объект командлету **Get-AzureAclConfig** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="43ef9-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43ef9-111">Этот командлет получает конфигурацию ACL для конечной точки с именем "веб".</span><span class="sxs-lookup"><span data-stu-id="43ef9-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="43ef9-112">Команда сохраняет этот объект конфигурации ACL в переменной $Acl.</span><span class="sxs-lookup"><span data-stu-id="43ef9-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="43ef9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43ef9-113">PARAMETERS</span></span>

### <span data-ttu-id="43ef9-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="43ef9-114">-EndpointName</span></span>
<span data-ttu-id="43ef9-115">Указывает имя конечной точки, для которой этот командлет получает ACL.</span><span class="sxs-lookup"><span data-stu-id="43ef9-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ef9-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="43ef9-116">-InformationAction</span></span>
<span data-ttu-id="43ef9-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="43ef9-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="43ef9-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43ef9-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43ef9-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="43ef9-119">Continue</span></span>
- <span data-ttu-id="43ef9-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="43ef9-120">Ignore</span></span>
- <span data-ttu-id="43ef9-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="43ef9-121">Inquire</span></span>
- <span data-ttu-id="43ef9-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="43ef9-122">SilentlyContinue</span></span>
- <span data-ttu-id="43ef9-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="43ef9-123">Stop</span></span>
- <span data-ttu-id="43ef9-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="43ef9-124">Suspend</span></span>

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

### <span data-ttu-id="43ef9-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="43ef9-125">-InformationVariable</span></span>
<span data-ttu-id="43ef9-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="43ef9-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="43ef9-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="43ef9-127">-Profile</span></span>
<span data-ttu-id="43ef9-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="43ef9-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43ef9-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43ef9-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43ef9-130">-VM</span><span class="sxs-lookup"><span data-stu-id="43ef9-130">-VM</span></span>
<span data-ttu-id="43ef9-131">Указывает объект виртуальной машины, для которого этот командлет получает конфигурацию ACL.</span><span class="sxs-lookup"><span data-stu-id="43ef9-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="43ef9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ef9-132">CommonParameters</span></span>
<span data-ttu-id="43ef9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43ef9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ef9-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ef9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ef9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43ef9-135">INPUTS</span></span>

## <span data-ttu-id="43ef9-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ef9-136">OUTPUTS</span></span>

## <span data-ttu-id="43ef9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="43ef9-137">NOTES</span></span>

## <span data-ttu-id="43ef9-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43ef9-138">RELATED LINKS</span></span>

[<span data-ttu-id="43ef9-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="43ef9-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="43ef9-140">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="43ef9-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="43ef9-141">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="43ef9-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="43ef9-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="43ef9-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


