---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567415"
---
# <span data-ttu-id="18b52-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18b52-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="18b52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18b52-102">SYNOPSIS</span></span>
<span data-ttu-id="18b52-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="18b52-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18b52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18b52-104">SYNTAX</span></span>

### <span data-ttu-id="18b52-105">GetAllPolicyDefinitions (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18b52-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="18b52-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="18b52-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="18b52-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="18b52-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="18b52-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18b52-108">DESCRIPTION</span></span>
<span data-ttu-id="18b52-109">Командлет **Get-AzureRmPolicyDefinition** получает все определения политик или определенную политику, определяемую именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="18b52-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="18b52-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18b52-110">EXAMPLES</span></span>

### <span data-ttu-id="18b52-111">Пример 1: получение определения политики</span><span class="sxs-lookup"><span data-stu-id="18b52-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="18b52-112">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="18b52-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="18b52-113">Пример 2: получение определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="18b52-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="18b52-114">Эта команда получает определение политики с именем VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="18b52-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="18b52-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18b52-115">PARAMETERS</span></span>

### <span data-ttu-id="18b52-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="18b52-116">-ApiVersion</span></span>
<span data-ttu-id="18b52-117">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18b52-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="18b52-118">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="18b52-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="18b52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b52-119">-DefaultProfile</span></span>
<span data-ttu-id="18b52-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="18b52-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18b52-121">-ID</span><span class="sxs-lookup"><span data-stu-id="18b52-121">-Id</span></span>
<span data-ttu-id="18b52-122">Указывает полный идентификатор ресурса для определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="18b52-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b52-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="18b52-123">-InformationAction</span></span>
<span data-ttu-id="18b52-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="18b52-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="18b52-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="18b52-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18b52-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="18b52-126">Continue</span></span>
- <span data-ttu-id="18b52-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="18b52-127">Ignore</span></span>
- <span data-ttu-id="18b52-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="18b52-128">Inquire</span></span>
- <span data-ttu-id="18b52-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="18b52-129">SilentlyContinue</span></span>
- <span data-ttu-id="18b52-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="18b52-130">Stop</span></span>
- <span data-ttu-id="18b52-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="18b52-131">Suspend</span></span>

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

### <span data-ttu-id="18b52-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="18b52-132">-InformationVariable</span></span>
<span data-ttu-id="18b52-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="18b52-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="18b52-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="18b52-134">-Name</span></span>
<span data-ttu-id="18b52-135">Указывает имя определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="18b52-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b52-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="18b52-136">-Pre</span></span>
<span data-ttu-id="18b52-137">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="18b52-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="18b52-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b52-138">CommonParameters</span></span>
<span data-ttu-id="18b52-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18b52-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b52-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b52-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b52-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18b52-141">INPUTS</span></span>

### <span data-ttu-id="18b52-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="18b52-142">None</span></span>
<span data-ttu-id="18b52-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="18b52-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18b52-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18b52-144">OUTPUTS</span></span>

### <span data-ttu-id="18b52-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="18b52-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="18b52-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="18b52-146">NOTES</span></span>

## <span data-ttu-id="18b52-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18b52-147">RELATED LINKS</span></span>

[<span data-ttu-id="18b52-148">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18b52-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="18b52-149">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18b52-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="18b52-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18b52-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


