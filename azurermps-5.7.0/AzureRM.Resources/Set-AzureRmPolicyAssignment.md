---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567933"
---
# <span data-ttu-id="bdb9d-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bdb9d-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="bdb9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdb9d-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb9d-103">Изменение назначения политики.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdb9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdb9d-104">SYNTAX</span></span>

### <span data-ttu-id="bdb9d-105">SetByPolicyAssignmentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bdb9d-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bdb9d-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="bdb9d-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bdb9d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdb9d-107">DESCRIPTION</span></span>
<span data-ttu-id="bdb9d-108">Командлет **Set-AzureRmPolicyAssignment** изменяет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="bdb9d-109">Укажите назначение по ИДЕНТИФИКАТОРу или по имени и области.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="bdb9d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdb9d-110">EXAMPLES</span></span>

### <span data-ttu-id="bdb9d-111">Пример 1: обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="bdb9d-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="bdb9d-112">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="bdb9d-113">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="bdb9d-114">Вторая команда получает назначение политики с именем PolicyAssignment с помощью командлета Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="bdb9d-115">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="bdb9d-116">Последняя команда обновляет отображаемое имя в назначении политики, определяемое свойством **ResourceId** для $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="bdb9d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdb9d-117">PARAMETERS</span></span>

### <span data-ttu-id="bdb9d-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bdb9d-118">-ApiVersion</span></span>
<span data-ttu-id="bdb9d-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bdb9d-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb9d-121">-DefaultProfile</span></span>
<span data-ttu-id="bdb9d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bdb9d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="bdb9d-123">-Description</span></span>
<span data-ttu-id="bdb9d-124">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="bdb9d-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bdb9d-125">-DisplayName</span></span>
<span data-ttu-id="bdb9d-126">Задает новое отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-127">-ID</span><span class="sxs-lookup"><span data-stu-id="bdb9d-127">-Id</span></span>
<span data-ttu-id="bdb9d-128">Указывает полный идентификатор ресурса для назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bdb9d-129">-InformationAction</span></span>
<span data-ttu-id="bdb9d-130">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bdb9d-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bdb9d-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bdb9d-132">Продолжал</span><span class="sxs-lookup"><span data-stu-id="bdb9d-132">Continue</span></span>
- <span data-ttu-id="bdb9d-133">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="bdb9d-133">Ignore</span></span>
- <span data-ttu-id="bdb9d-134">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="bdb9d-134">Inquire</span></span>
- <span data-ttu-id="bdb9d-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bdb9d-135">SilentlyContinue</span></span>
- <span data-ttu-id="bdb9d-136">Остановить</span><span class="sxs-lookup"><span data-stu-id="bdb9d-136">Stop</span></span>
- <span data-ttu-id="bdb9d-137">Рвать</span><span class="sxs-lookup"><span data-stu-id="bdb9d-137">Suspend</span></span>

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

### <span data-ttu-id="bdb9d-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bdb9d-138">-InformationVariable</span></span>
<span data-ttu-id="bdb9d-139">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bdb9d-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bdb9d-140">-Name</span></span>
<span data-ttu-id="bdb9d-141">Указывает имя назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="bdb9d-142">-NotScope</span></span>
<span data-ttu-id="bdb9d-143">Назначение политики не является областью действия.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="bdb9d-144">-Pre</span></span>
<span data-ttu-id="bdb9d-145">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-146">-Scope</span><span class="sxs-lookup"><span data-stu-id="bdb9d-146">-Scope</span></span>
<span data-ttu-id="bdb9d-147">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="bdb9d-148">-Sku</span></span>
<span data-ttu-id="bdb9d-149">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb9d-150">CommonParameters</span></span>
<span data-ttu-id="bdb9d-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb9d-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb9d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb9d-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdb9d-153">INPUTS</span></span>

### <span data-ttu-id="bdb9d-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="bdb9d-154">None</span></span>
<span data-ttu-id="bdb9d-155">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bdb9d-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bdb9d-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdb9d-156">OUTPUTS</span></span>

### <span data-ttu-id="bdb9d-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bdb9d-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bdb9d-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdb9d-158">NOTES</span></span>

## <span data-ttu-id="bdb9d-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdb9d-159">RELATED LINKS</span></span>

[<span data-ttu-id="bdb9d-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bdb9d-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="bdb9d-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bdb9d-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="bdb9d-162">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bdb9d-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


