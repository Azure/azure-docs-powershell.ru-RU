---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733552"
---
# <span data-ttu-id="c8bfd-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8bfd-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="c8bfd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bfd-103">Получение назначений политики.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8bfd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8bfd-104">SYNTAX</span></span>

### <span data-ttu-id="c8bfd-105">GetAllPolicyAssignments (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8bfd-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c8bfd-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c8bfd-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c8bfd-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="c8bfd-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8bfd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8bfd-108">DESCRIPTION</span></span>
<span data-ttu-id="c8bfd-109">Командлет **Get-AzureRmPolicyAssignment** получает все назначения политик или конкретные назначения.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="c8bfd-110">Определите назначение политики для получения имени и области или по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="c8bfd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8bfd-111">EXAMPLES</span></span>

### <span data-ttu-id="c8bfd-112">Пример 1: получение всех назначений политики</span><span class="sxs-lookup"><span data-stu-id="c8bfd-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="c8bfd-113">Эта команда получает все назначения политики.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="c8bfd-114">Пример 2: получение определенного назначения политики</span><span class="sxs-lookup"><span data-stu-id="c8bfd-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c8bfd-115">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="c8bfd-116">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="c8bfd-117">Вторая команда получает назначение политики с именем PolicyAssignment07 для области, которой идентифицировано свойство **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="c8bfd-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8bfd-118">PARAMETERS</span></span>

### <span data-ttu-id="c8bfd-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8bfd-119">-ApiVersion</span></span>
<span data-ttu-id="c8bfd-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c8bfd-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c8bfd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bfd-122">-DefaultProfile</span></span>
<span data-ttu-id="c8bfd-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c8bfd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8bfd-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c8bfd-124">-Id</span></span>
<span data-ttu-id="c8bfd-125">Указывает полный идентификатор ресурса для назначения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bfd-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8bfd-126">-InformationAction</span></span>
<span data-ttu-id="c8bfd-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8bfd-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c8bfd-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8bfd-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c8bfd-129">Continue</span></span>
- <span data-ttu-id="c8bfd-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c8bfd-130">Ignore</span></span>
- <span data-ttu-id="c8bfd-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c8bfd-131">Inquire</span></span>
- <span data-ttu-id="c8bfd-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8bfd-132">SilentlyContinue</span></span>
- <span data-ttu-id="c8bfd-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="c8bfd-133">Stop</span></span>
- <span data-ttu-id="c8bfd-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="c8bfd-134">Suspend</span></span>

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

### <span data-ttu-id="c8bfd-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8bfd-135">-InformationVariable</span></span>
<span data-ttu-id="c8bfd-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c8bfd-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8bfd-137">-Name</span></span>
<span data-ttu-id="c8bfd-138">Указывает имя назначения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bfd-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c8bfd-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="c8bfd-140">Указывает идентификатор определения политики для назначений политики, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bfd-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="c8bfd-141">-Pre</span></span>
<span data-ttu-id="c8bfd-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c8bfd-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="c8bfd-143">-Scope</span></span>
<span data-ttu-id="c8bfd-144">Указывает область, в которой применяется политика для задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bfd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bfd-145">CommonParameters</span></span>
<span data-ttu-id="c8bfd-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bfd-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8bfd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bfd-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8bfd-148">INPUTS</span></span>

### <span data-ttu-id="c8bfd-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="c8bfd-149">None</span></span>
<span data-ttu-id="c8bfd-150">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8bfd-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8bfd-151">OUTPUTS</span></span>

### <span data-ttu-id="c8bfd-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c8bfd-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c8bfd-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8bfd-153">NOTES</span></span>

## <span data-ttu-id="c8bfd-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8bfd-154">RELATED LINKS</span></span>

[<span data-ttu-id="c8bfd-155">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8bfd-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c8bfd-156">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8bfd-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c8bfd-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8bfd-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


