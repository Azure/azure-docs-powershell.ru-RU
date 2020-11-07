---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733631"
---
# <span data-ttu-id="23f9e-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="23f9e-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="23f9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="23f9e-103">Создание назначения политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23f9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23f9e-104">SYNTAX</span></span>

### <span data-ttu-id="23f9e-105">Назначение политики без параметров (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23f9e-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23f9e-106">Назначение политики с параметрами с помощью объекта параметра политики</span><span class="sxs-lookup"><span data-stu-id="23f9e-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23f9e-107">Назначение политики с параметрами с помощью строки параметра политики</span><span class="sxs-lookup"><span data-stu-id="23f9e-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23f9e-108">Назначение политики с параметрами с помощью объекта параметров SET политики</span><span class="sxs-lookup"><span data-stu-id="23f9e-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23f9e-109">Назначение политики с параметрами с помощью строки параметров SET политики</span><span class="sxs-lookup"><span data-stu-id="23f9e-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23f9e-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23f9e-110">DESCRIPTION</span></span>
<span data-ttu-id="23f9e-111">Командлет **New-AzureRmPolicyAssignment** создает назначение политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="23f9e-112">Укажите политику и область действия.</span><span class="sxs-lookup"><span data-stu-id="23f9e-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="23f9e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23f9e-113">EXAMPLES</span></span>

### <span data-ttu-id="23f9e-114">Пример 1: назначение политики на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="23f9e-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="23f9e-115">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="23f9e-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="23f9e-116">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="23f9e-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="23f9e-117">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="23f9e-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="23f9e-118">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="23f9e-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="23f9e-119">Последняя команда назначает политику в $Policy на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23f9e-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="23f9e-120">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23f9e-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="23f9e-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23f9e-121">PARAMETERS</span></span>

### <span data-ttu-id="23f9e-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23f9e-122">-ApiVersion</span></span>
<span data-ttu-id="23f9e-123">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23f9e-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="23f9e-124">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="23f9e-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="23f9e-125">-DisplayName</span></span>
<span data-ttu-id="23f9e-126">Задает отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-126">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23f9e-127">-InformationAction</span></span>
<span data-ttu-id="23f9e-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="23f9e-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23f9e-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="23f9e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23f9e-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="23f9e-130">Continue</span></span>
- <span data-ttu-id="23f9e-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="23f9e-131">Ignore</span></span>
- <span data-ttu-id="23f9e-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="23f9e-132">Inquire</span></span>
- <span data-ttu-id="23f9e-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23f9e-133">SilentlyContinue</span></span>
- <span data-ttu-id="23f9e-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="23f9e-134">Stop</span></span>
- <span data-ttu-id="23f9e-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="23f9e-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23f9e-136">-InformationVariable</span></span>
<span data-ttu-id="23f9e-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="23f9e-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23f9e-138">-Name</span></span>
<span data-ttu-id="23f9e-139">Задает имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-139">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="23f9e-140">-NotScope</span></span>
<span data-ttu-id="23f9e-141">Область "не для назначения политики".</span><span class="sxs-lookup"><span data-stu-id="23f9e-141">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23f9e-142">-PolicyDefinition</span></span>
<span data-ttu-id="23f9e-143">Указывает политику, как объект **PSObject** , который содержит правило политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="23f9e-144">-PolicyParameter</span></span>
<span data-ttu-id="23f9e-145">Путь к файлу параметра политики или строка параметра политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="23f9e-146">-PolicyParameterObject</span></span>
<span data-ttu-id="23f9e-147">Объект параметра политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="23f9e-148">-PolicySetDefinition</span></span>
<span data-ttu-id="23f9e-149">Объект определения параметра политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="23f9e-150">-Pre</span></span>
<span data-ttu-id="23f9e-151">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="23f9e-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="23f9e-152">-Scope</span></span>
<span data-ttu-id="23f9e-153">Указывает область, в которой нужно назначить политику.</span><span class="sxs-lookup"><span data-stu-id="23f9e-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="23f9e-154">Например, чтобы назначить политику группе ресурсов, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="23f9e-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="23f9e-155">`/subscriptions/``/resourcegroups/`имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="23f9e-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f9e-156">-DefaultProfile</span></span>
<span data-ttu-id="23f9e-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23f9e-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-158">-Описание</span><span class="sxs-lookup"><span data-stu-id="23f9e-158">-Description</span></span>
<span data-ttu-id="23f9e-159">Описание назначения политики.</span><span class="sxs-lookup"><span data-stu-id="23f9e-159">The description for policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="23f9e-160">-Sku</span></span>
<span data-ttu-id="23f9e-161">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="23f9e-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="23f9e-162">По умолчанию для освобождения SKU: Name = a0, Tiering = Free (бесплатно)</span><span class="sxs-lookup"><span data-stu-id="23f9e-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f9e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f9e-163">CommonParameters</span></span>
<span data-ttu-id="23f9e-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23f9e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f9e-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f9e-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f9e-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23f9e-166">INPUTS</span></span>

## <span data-ttu-id="23f9e-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23f9e-167">OUTPUTS</span></span>

### <span data-ttu-id="23f9e-168">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="23f9e-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="23f9e-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="23f9e-169">NOTES</span></span>

## <span data-ttu-id="23f9e-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23f9e-170">RELATED LINKS</span></span>

[<span data-ttu-id="23f9e-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23f9e-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="23f9e-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="23f9e-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="23f9e-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="23f9e-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="23f9e-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="23f9e-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


