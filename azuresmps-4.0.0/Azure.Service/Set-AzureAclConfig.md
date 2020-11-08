---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076432"
---
# <span data-ttu-id="f3793-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f3793-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="f3793-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3793-102">SYNOPSIS</span></span>
<span data-ttu-id="f3793-103">Изменяет объект конфигурации ACL.</span><span class="sxs-lookup"><span data-stu-id="f3793-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="f3793-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3793-104">SYNTAX</span></span>

### <span data-ttu-id="f3793-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="f3793-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3793-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="f3793-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3793-107">SetRule</span><span class="sxs-lookup"><span data-stu-id="f3793-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f3793-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3793-108">DESCRIPTION</span></span>
<span data-ttu-id="f3793-109">Командлет **Set-AzureAclConfig** изменяет объект конфигурации списка управления доступом (ACL) из существующей конфигурации виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="f3793-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="f3793-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3793-110">EXAMPLES</span></span>

### <span data-ttu-id="f3793-111">Пример 1: Добавление правила в новую конфигурацию ACL</span><span class="sxs-lookup"><span data-stu-id="f3793-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="f3793-112">Первая команда создает конфигурацию ACL и сохраняет ее в переменной $Acl.</span><span class="sxs-lookup"><span data-stu-id="f3793-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="f3793-113">Вторая команда добавляет новое правило к конфигурации, хранящейся в $Acl.</span><span class="sxs-lookup"><span data-stu-id="f3793-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="f3793-114">Команда задает действие, подсеть, порядок и описание для правила.</span><span class="sxs-lookup"><span data-stu-id="f3793-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="f3793-115">Пример 2: изменение правила в конфигурации ACL</span><span class="sxs-lookup"><span data-stu-id="f3793-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="f3793-116">Первая команда получает виртуальную машину с именем VirtualMachine07 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f3793-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f3793-117">Команда передает этот объект командлету **Get-AzureAclConfig** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f3793-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3793-118">Этот командлет получает конфигурацию ACL для конечной точки с именем "веб".</span><span class="sxs-lookup"><span data-stu-id="f3793-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="f3793-119">Команда сохраняет этот объект конфигурации ACL в переменной $Acl.</span><span class="sxs-lookup"><span data-stu-id="f3793-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="f3793-120">Вторая команда изменяет правило с ИДЕНТИФИКАТОРом 0.</span><span class="sxs-lookup"><span data-stu-id="f3793-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="f3793-121">Эта команда изменяет порядок и описание правила.</span><span class="sxs-lookup"><span data-stu-id="f3793-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="f3793-122">Последняя команда задает объект конфигурации ACL для виртуальной машины с помощью командлета **Set-AzureEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="f3793-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="f3793-123">Кроме того, команда обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f3793-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="f3793-124">Пример 3: Удаление правила из конфигурации ACL</span><span class="sxs-lookup"><span data-stu-id="f3793-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="f3793-125">Первая команда сохраняет объект конфигурации ACL в переменной $Acl.</span><span class="sxs-lookup"><span data-stu-id="f3793-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="f3793-126">Это то же самое, что и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="f3793-126">This is the same as the previous example.</span></span>

<span data-ttu-id="f3793-127">Вторая команда удаляет правило с ИДЕНТИФИКАТОРом 0 из конфигурации ACL в $Acl.</span><span class="sxs-lookup"><span data-stu-id="f3793-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="f3793-128">Последняя команда задает объект конфигурации ACL для виртуальной машины и обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f3793-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="f3793-129">Это то же самое, что и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="f3793-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="f3793-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3793-130">PARAMETERS</span></span>

### <span data-ttu-id="f3793-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="f3793-131">-ACL</span></span>
<span data-ttu-id="f3793-132">Указывает объект конфигурации ACL, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3793-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-133">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="f3793-133">-Action</span></span>
<span data-ttu-id="f3793-134">Задает действие для правила, которое добавляет или изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3793-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="f3793-135">Допустимые значения: Permit и Deny.</span><span class="sxs-lookup"><span data-stu-id="f3793-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="f3793-136">-AddRule</span></span>
<span data-ttu-id="f3793-137">Указывает на то, что этот командлет добавляет правило к конфигурации ACL.</span><span class="sxs-lookup"><span data-stu-id="f3793-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-138">-Описание</span><span class="sxs-lookup"><span data-stu-id="f3793-138">-Description</span></span>
<span data-ttu-id="f3793-139">Задает описание для правила, которое добавляет или изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3793-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f3793-140">-InformationAction</span></span>
<span data-ttu-id="f3793-141">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f3793-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f3793-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f3793-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3793-143">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f3793-143">Continue</span></span>
- <span data-ttu-id="f3793-144">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f3793-144">Ignore</span></span>
- <span data-ttu-id="f3793-145">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f3793-145">Inquire</span></span>
- <span data-ttu-id="f3793-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f3793-146">SilentlyContinue</span></span>
- <span data-ttu-id="f3793-147">Остановить</span><span class="sxs-lookup"><span data-stu-id="f3793-147">Stop</span></span>
- <span data-ttu-id="f3793-148">Рвать</span><span class="sxs-lookup"><span data-stu-id="f3793-148">Suspend</span></span>

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

### <span data-ttu-id="f3793-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f3793-149">-InformationVariable</span></span>
<span data-ttu-id="f3793-150">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f3793-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f3793-151">-Порядок</span><span class="sxs-lookup"><span data-stu-id="f3793-151">-Order</span></span>
<span data-ttu-id="f3793-152">Указывает порядок обработки для правила, которое добавляет или изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3793-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="f3793-153">-RemoteSubnet</span></span>
<span data-ttu-id="f3793-154">Указывает удаленную подсеть для правила, которое добавляет или изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3793-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="f3793-155">Указывает адрес в формате бездоменной маршрутизации (CIDR) класса.</span><span class="sxs-lookup"><span data-stu-id="f3793-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="f3793-156">-RemoveRule</span></span>
<span data-ttu-id="f3793-157">Указывает на то, что этот командлет удаляет правило из конфигурации ACL.</span><span class="sxs-lookup"><span data-stu-id="f3793-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="f3793-158">-RuleId</span></span>
<span data-ttu-id="f3793-159">Указывает идентификатор правила, которое этот командлет удаляет или изменяет для конфигурации ACL.</span><span class="sxs-lookup"><span data-stu-id="f3793-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-160">-SetRule</span><span class="sxs-lookup"><span data-stu-id="f3793-160">-SetRule</span></span>
<span data-ttu-id="f3793-161">Указывает на то, что этот командлет изменяет правило в конфигурации ACL.</span><span class="sxs-lookup"><span data-stu-id="f3793-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3793-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3793-162">CommonParameters</span></span>
<span data-ttu-id="f3793-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3793-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3793-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3793-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3793-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3793-165">INPUTS</span></span>

## <span data-ttu-id="f3793-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3793-166">OUTPUTS</span></span>

## <span data-ttu-id="f3793-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3793-167">NOTES</span></span>

## <span data-ttu-id="f3793-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3793-168">RELATED LINKS</span></span>

[<span data-ttu-id="f3793-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f3793-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="f3793-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f3793-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f3793-171">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f3793-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="f3793-172">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f3793-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="f3793-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3793-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="f3793-174">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f3793-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


