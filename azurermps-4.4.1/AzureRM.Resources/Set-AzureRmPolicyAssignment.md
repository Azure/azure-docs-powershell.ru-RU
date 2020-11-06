---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562187"
---
# <span data-ttu-id="cc7b7-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="cc7b7-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="cc7b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7b7-103">Изменение назначения политики.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc7b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc7b7-104">SYNTAX</span></span>

### <span data-ttu-id="cc7b7-105">Заданный параметр имени назначения политики.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="cc7b7-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cc7b7-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cc7b7-107">Заданный параметр идентификатора назначения политики.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cc7b7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc7b7-108">DESCRIPTION</span></span>
<span data-ttu-id="cc7b7-109">Командлет **Set-AzureRmPolicyAssignment** изменяет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="cc7b7-110">Укажите назначение по ИДЕНТИФИКАТОРу или по имени и области.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="cc7b7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc7b7-111">EXAMPLES</span></span>

### <span data-ttu-id="cc7b7-112">Пример 1: обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="cc7b7-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="cc7b7-113">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="cc7b7-114">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="cc7b7-115">Вторая команда получает назначение политики с именем PolicyAssignment с помощью командлета Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="cc7b7-116">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="cc7b7-117">Последняя команда обновляет отображаемое имя в назначении политики, определяемое свойством **ResourceId** для $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="cc7b7-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc7b7-118">PARAMETERS</span></span>

### <span data-ttu-id="cc7b7-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cc7b7-119">-ApiVersion</span></span>
<span data-ttu-id="cc7b7-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cc7b7-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cc7b7-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc7b7-122">-DisplayName</span></span>
<span data-ttu-id="cc7b7-123">Задает новое отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-123">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="cc7b7-124">-ID</span><span class="sxs-lookup"><span data-stu-id="cc7b7-124">-Id</span></span>
<span data-ttu-id="cc7b7-125">Указывает полный идентификатор ресурса для назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7b7-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cc7b7-126">-InformationAction</span></span>
<span data-ttu-id="cc7b7-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cc7b7-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cc7b7-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc7b7-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="cc7b7-129">Continue</span></span>
- <span data-ttu-id="cc7b7-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="cc7b7-130">Ignore</span></span>
- <span data-ttu-id="cc7b7-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="cc7b7-131">Inquire</span></span>
- <span data-ttu-id="cc7b7-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cc7b7-132">SilentlyContinue</span></span>
- <span data-ttu-id="cc7b7-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="cc7b7-133">Stop</span></span>
- <span data-ttu-id="cc7b7-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="cc7b7-134">Suspend</span></span>

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

### <span data-ttu-id="cc7b7-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cc7b7-135">-InformationVariable</span></span>
<span data-ttu-id="cc7b7-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cc7b7-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc7b7-137">-Name</span></span>
<span data-ttu-id="cc7b7-138">Указывает имя назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7b7-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="cc7b7-139">-NotScope</span></span>
<span data-ttu-id="cc7b7-140">Назначение политики не является областью действия.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7b7-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="cc7b7-141">-Pre</span></span>
<span data-ttu-id="cc7b7-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cc7b7-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="cc7b7-143">-Scope</span></span>
<span data-ttu-id="cc7b7-144">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7b7-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7b7-145">-DefaultProfile</span></span>
<span data-ttu-id="cc7b7-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc7b7-147">-Описание</span><span class="sxs-lookup"><span data-stu-id="cc7b7-147">-Description</span></span>
<span data-ttu-id="cc7b7-148">Описание назначения политики.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-148">The description for policy assignment.</span></span>

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

### <span data-ttu-id="cc7b7-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="cc7b7-149">-Sku</span></span>
<span data-ttu-id="cc7b7-150">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-150">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="cc7b7-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7b7-151">CommonParameters</span></span>
<span data-ttu-id="cc7b7-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc7b7-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7b7-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc7b7-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7b7-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc7b7-154">INPUTS</span></span>

## <span data-ttu-id="cc7b7-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc7b7-155">OUTPUTS</span></span>

### <span data-ttu-id="cc7b7-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cc7b7-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cc7b7-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc7b7-157">NOTES</span></span>

## <span data-ttu-id="cc7b7-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc7b7-158">RELATED LINKS</span></span>

[<span data-ttu-id="cc7b7-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="cc7b7-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="cc7b7-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="cc7b7-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="cc7b7-161">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="cc7b7-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


