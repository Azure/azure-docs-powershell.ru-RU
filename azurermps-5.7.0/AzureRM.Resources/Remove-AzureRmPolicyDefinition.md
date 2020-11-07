---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732142"
---
# <span data-ttu-id="ed463-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ed463-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="ed463-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed463-102">SYNOPSIS</span></span>
<span data-ttu-id="ed463-103">Удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="ed463-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed463-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed463-104">SYNTAX</span></span>

### <span data-ttu-id="ed463-105">RemoveByPolicyDefinitionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed463-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed463-106">RemoveByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ed463-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed463-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed463-107">DESCRIPTION</span></span>
<span data-ttu-id="ed463-108">Командлет **Remove-AzureRmPolicyDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="ed463-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="ed463-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed463-109">EXAMPLES</span></span>

### <span data-ttu-id="ed463-110">Пример 1: Удаление определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="ed463-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="ed463-111">Эта команда удаляет указанное определение политики.</span><span class="sxs-lookup"><span data-stu-id="ed463-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="ed463-112">Пример 2: Удаление определения политики по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="ed463-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="ed463-113">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ed463-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ed463-114">Команда сохраняет его в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ed463-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="ed463-115">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ed463-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="ed463-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed463-116">PARAMETERS</span></span>

### <span data-ttu-id="ed463-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ed463-117">-ApiVersion</span></span>
<span data-ttu-id="ed463-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed463-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ed463-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="ed463-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ed463-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed463-120">-DefaultProfile</span></span>
<span data-ttu-id="ed463-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed463-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed463-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ed463-122">-Force</span></span>
<span data-ttu-id="ed463-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed463-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed463-124">-ID</span><span class="sxs-lookup"><span data-stu-id="ed463-124">-Id</span></span>
<span data-ttu-id="ed463-125">Указывает полный идентификатор ресурса для определения политики, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ed463-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed463-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ed463-126">-InformationAction</span></span>
<span data-ttu-id="ed463-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="ed463-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ed463-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ed463-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed463-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="ed463-129">Continue</span></span>
- <span data-ttu-id="ed463-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="ed463-130">Ignore</span></span>
- <span data-ttu-id="ed463-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="ed463-131">Inquire</span></span>
- <span data-ttu-id="ed463-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ed463-132">SilentlyContinue</span></span>
- <span data-ttu-id="ed463-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="ed463-133">Stop</span></span>
- <span data-ttu-id="ed463-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="ed463-134">Suspend</span></span>

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

### <span data-ttu-id="ed463-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ed463-135">-InformationVariable</span></span>
<span data-ttu-id="ed463-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="ed463-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ed463-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed463-137">-Name</span></span>
<span data-ttu-id="ed463-138">Указывает имя определения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ed463-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed463-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="ed463-139">-Pre</span></span>
<span data-ttu-id="ed463-140">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="ed463-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ed463-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed463-141">-Confirm</span></span>
<span data-ttu-id="ed463-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed463-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed463-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed463-143">-WhatIf</span></span>
<span data-ttu-id="ed463-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed463-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed463-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed463-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed463-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed463-146">CommonParameters</span></span>
<span data-ttu-id="ed463-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed463-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed463-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed463-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed463-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed463-149">INPUTS</span></span>

### <span data-ttu-id="ed463-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed463-150">None</span></span>
<span data-ttu-id="ed463-151">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ed463-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed463-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed463-152">OUTPUTS</span></span>

### <span data-ttu-id="ed463-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed463-153">System.Boolean</span></span>

## <span data-ttu-id="ed463-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed463-154">NOTES</span></span>

## <span data-ttu-id="ed463-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed463-155">RELATED LINKS</span></span>

[<span data-ttu-id="ed463-156">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ed463-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="ed463-157">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ed463-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="ed463-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ed463-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


