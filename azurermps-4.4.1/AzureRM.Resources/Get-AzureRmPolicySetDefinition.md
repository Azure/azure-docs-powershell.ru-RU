---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567090"
---
# <span data-ttu-id="ef6a7-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ef6a7-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="ef6a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6a7-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef6a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef6a7-104">SYNTAX</span></span>

### <span data-ttu-id="ef6a7-105">Список всех наборов параметров определений политики.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="ef6a7-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ef6a7-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6a7-107">Параметр имени определения политики задает.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef6a7-108">Параметр идентификатора определения политики задает значение.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef6a7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef6a7-109">DESCRIPTION</span></span>
<span data-ttu-id="ef6a7-110">Командлет **Get-AzureRmPolicySetDefinition** получает все определения политики или определенную политику, определяемую именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="ef6a7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef6a7-111">EXAMPLES</span></span>

### <span data-ttu-id="ef6a7-112">Пример 1: получение определения множества политик</span><span class="sxs-lookup"><span data-stu-id="ef6a7-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="ef6a7-113">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="ef6a7-114">Пример 2: получение определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="ef6a7-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="ef6a7-115">Эта команда получает определение политики с именем VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="ef6a7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef6a7-116">PARAMETERS</span></span>

### <span data-ttu-id="ef6a7-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef6a7-117">-ApiVersion</span></span>
<span data-ttu-id="ef6a7-118">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef6a7-119">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ef6a7-120">-ID</span><span class="sxs-lookup"><span data-stu-id="ef6a7-120">-Id</span></span>
<span data-ttu-id="ef6a7-121">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="ef6a7-122">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ef6a7-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef6a7-123">-Name</span></span>
<span data-ttu-id="ef6a7-124">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a7-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="ef6a7-125">-Pre</span></span>
<span data-ttu-id="ef6a7-126">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ef6a7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6a7-127">-DefaultProfile</span></span>
<span data-ttu-id="ef6a7-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef6a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6a7-129">CommonParameters</span></span>
<span data-ttu-id="ef6a7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef6a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6a7-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef6a7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6a7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef6a7-132">INPUTS</span></span>

### <span data-ttu-id="ef6a7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ef6a7-133">System.String</span></span>

## <span data-ttu-id="ef6a7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef6a7-134">OUTPUTS</span></span>

### <span data-ttu-id="ef6a7-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ef6a7-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ef6a7-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef6a7-136">NOTES</span></span>

## <span data-ttu-id="ef6a7-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef6a7-137">RELATED LINKS</span></span>

