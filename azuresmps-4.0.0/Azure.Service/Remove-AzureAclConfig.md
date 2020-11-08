---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076175"
---
# <span data-ttu-id="0c50f-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0c50f-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="0c50f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c50f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c50f-103">Удаляет объект конфигурации ACL из конфигурации виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="0c50f-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="0c50f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c50f-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0c50f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c50f-105">DESCRIPTION</span></span>
<span data-ttu-id="0c50f-106">Командлет **Remove-AzureAclConfig** удаляет объект конфигурации списка управления доступом (ACL) из конфигурации виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="0c50f-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="0c50f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c50f-107">EXAMPLES</span></span>

### <span data-ttu-id="0c50f-108">Пример 1: Удаление конфигурации ACL</span><span class="sxs-lookup"><span data-stu-id="0c50f-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="0c50f-109">Эта команда получает виртуальную машину с именем VirtualMachine07 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="0c50f-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="0c50f-110">Команда передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0c50f-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0c50f-111">Этот командлет удаляет конфигурацию ACL для конечной точки с именем "веб".</span><span class="sxs-lookup"><span data-stu-id="0c50f-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="0c50f-112">Команда передает результат в командлет **Update-AzureVM** , который обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0c50f-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="0c50f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c50f-113">PARAMETERS</span></span>

### <span data-ttu-id="0c50f-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0c50f-114">-EndpointName</span></span>
<span data-ttu-id="0c50f-115">Указывает имя конечной точки, из которой этот командлет удаляет конфигурацию ACL.</span><span class="sxs-lookup"><span data-stu-id="0c50f-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c50f-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0c50f-116">-InformationAction</span></span>
<span data-ttu-id="0c50f-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="0c50f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0c50f-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0c50f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c50f-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="0c50f-119">Continue</span></span>
- <span data-ttu-id="0c50f-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="0c50f-120">Ignore</span></span>
- <span data-ttu-id="0c50f-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="0c50f-121">Inquire</span></span>
- <span data-ttu-id="0c50f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0c50f-122">SilentlyContinue</span></span>
- <span data-ttu-id="0c50f-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="0c50f-123">Stop</span></span>
- <span data-ttu-id="0c50f-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="0c50f-124">Suspend</span></span>

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

### <span data-ttu-id="0c50f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0c50f-125">-InformationVariable</span></span>
<span data-ttu-id="0c50f-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="0c50f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0c50f-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="0c50f-127">-Profile</span></span>
<span data-ttu-id="0c50f-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0c50f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c50f-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0c50f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c50f-130">-VM</span><span class="sxs-lookup"><span data-stu-id="0c50f-130">-VM</span></span>
<span data-ttu-id="0c50f-131">Указывает виртуальную машину, с которой этот командлет удаляет конфигурацию ACL.</span><span class="sxs-lookup"><span data-stu-id="0c50f-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

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

### <span data-ttu-id="0c50f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c50f-132">CommonParameters</span></span>
<span data-ttu-id="0c50f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c50f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c50f-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c50f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c50f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c50f-135">INPUTS</span></span>

## <span data-ttu-id="0c50f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c50f-136">OUTPUTS</span></span>

## <span data-ttu-id="0c50f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c50f-137">NOTES</span></span>

## <span data-ttu-id="0c50f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c50f-138">RELATED LINKS</span></span>

[<span data-ttu-id="0c50f-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0c50f-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="0c50f-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0c50f-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="0c50f-141">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0c50f-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="0c50f-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0c50f-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="0c50f-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0c50f-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


