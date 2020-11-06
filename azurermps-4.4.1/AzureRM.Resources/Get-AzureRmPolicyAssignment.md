---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562191"
---
# <span data-ttu-id="5cd10-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5cd10-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="5cd10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5cd10-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd10-103">Получение назначений политики.</span><span class="sxs-lookup"><span data-stu-id="5cd10-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cd10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5cd10-104">SYNTAX</span></span>

### <span data-ttu-id="5cd10-105">Список всех наборов параметров назначений политики.</span><span class="sxs-lookup"><span data-stu-id="5cd10-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="5cd10-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="5cd10-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5cd10-107">Заданный параметр имени назначения политики.</span><span class="sxs-lookup"><span data-stu-id="5cd10-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5cd10-108">Заданный параметр идентификатора назначения политики.</span><span class="sxs-lookup"><span data-stu-id="5cd10-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5cd10-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cd10-109">DESCRIPTION</span></span>
<span data-ttu-id="5cd10-110">Командлет **Get-AzureRmPolicyAssignment** получает все назначения политик или конкретные назначения.</span><span class="sxs-lookup"><span data-stu-id="5cd10-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="5cd10-111">Определите назначение политики для получения имени и области или по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="5cd10-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="5cd10-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5cd10-112">EXAMPLES</span></span>

### <span data-ttu-id="5cd10-113">Пример 1: получение всех назначений политики</span><span class="sxs-lookup"><span data-stu-id="5cd10-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="5cd10-114">Эта команда получает все назначения политики.</span><span class="sxs-lookup"><span data-stu-id="5cd10-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="5cd10-115">Пример 2: получение определенного назначения политики</span><span class="sxs-lookup"><span data-stu-id="5cd10-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="5cd10-116">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5cd10-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="5cd10-117">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5cd10-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="5cd10-118">Вторая команда получает назначение политики с именем PolicyAssignment07 для области, которой идентифицировано свойство **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5cd10-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="5cd10-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5cd10-119">PARAMETERS</span></span>

### <span data-ttu-id="5cd10-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5cd10-120">-ApiVersion</span></span>
<span data-ttu-id="5cd10-121">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cd10-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5cd10-122">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="5cd10-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5cd10-123">-ID</span><span class="sxs-lookup"><span data-stu-id="5cd10-123">-Id</span></span>
<span data-ttu-id="5cd10-124">Указывает полный идентификатор ресурса для назначения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5cd10-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5cd10-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5cd10-125">-InformationAction</span></span>
<span data-ttu-id="5cd10-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="5cd10-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5cd10-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5cd10-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cd10-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="5cd10-128">Continue</span></span>
- <span data-ttu-id="5cd10-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="5cd10-129">Ignore</span></span>
- <span data-ttu-id="5cd10-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="5cd10-130">Inquire</span></span>
- <span data-ttu-id="5cd10-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5cd10-131">SilentlyContinue</span></span>
- <span data-ttu-id="5cd10-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="5cd10-132">Stop</span></span>
- <span data-ttu-id="5cd10-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="5cd10-133">Suspend</span></span>

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

### <span data-ttu-id="5cd10-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5cd10-134">-InformationVariable</span></span>
<span data-ttu-id="5cd10-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="5cd10-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5cd10-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5cd10-136">-Name</span></span>
<span data-ttu-id="5cd10-137">Указывает имя назначения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5cd10-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd10-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5cd10-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="5cd10-139">Указывает идентификатор определения политики для назначений политики, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5cd10-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd10-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="5cd10-140">-Pre</span></span>
<span data-ttu-id="5cd10-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="5cd10-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5cd10-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="5cd10-142">-Scope</span></span>
<span data-ttu-id="5cd10-143">Указывает область, в которой применяется политика для задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5cd10-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5cd10-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd10-144">-DefaultProfile</span></span>
<span data-ttu-id="5cd10-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd10-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cd10-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd10-146">CommonParameters</span></span>
<span data-ttu-id="5cd10-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5cd10-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd10-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd10-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd10-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5cd10-149">INPUTS</span></span>

## <span data-ttu-id="5cd10-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cd10-150">OUTPUTS</span></span>

### <span data-ttu-id="5cd10-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5cd10-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5cd10-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="5cd10-152">NOTES</span></span>

## <span data-ttu-id="5cd10-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cd10-153">RELATED LINKS</span></span>

[<span data-ttu-id="5cd10-154">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5cd10-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="5cd10-155">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5cd10-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="5cd10-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5cd10-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


