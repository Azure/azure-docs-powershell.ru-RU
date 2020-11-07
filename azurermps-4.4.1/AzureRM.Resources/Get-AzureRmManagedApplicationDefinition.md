---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ef724c4d2e9771243058471c3ce2aebc944d2bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732412"
---
# <span data-ttu-id="8298f-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="8298f-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="8298f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8298f-102">SYNOPSIS</span></span>
<span data-ttu-id="8298f-103">Получение определений управляемых приложений</span><span class="sxs-lookup"><span data-stu-id="8298f-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8298f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8298f-104">SYNTAX</span></span>

### <span data-ttu-id="8298f-105">Заданный параметр имени определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8298f-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="8298f-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8298f-106">(Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8298f-107">Заданный параметр идентификатора определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8298f-107">The managed application definition Id parameter set.</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8298f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8298f-108">DESCRIPTION</span></span>
<span data-ttu-id="8298f-109">Командлет **Get-AzureRmManagedApplicationDefinition** получает определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="8298f-109">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="8298f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8298f-110">EXAMPLES</span></span>

### <span data-ttu-id="8298f-111">Пример 1: получение всех определений управляемых приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="8298f-111">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="8298f-112">Эта команда получает определения управляемых приложений в группе ресурсов "MyRG".</span><span class="sxs-lookup"><span data-stu-id="8298f-112">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="8298f-113">Пример 2: получение определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="8298f-113">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="8298f-114">Эта команда получает определение управляемого приложения "myManagedAppDef" в разделе "Группа ресурсов" MyRG "</span><span class="sxs-lookup"><span data-stu-id="8298f-114">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="8298f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8298f-115">PARAMETERS</span></span>

### <span data-ttu-id="8298f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8298f-116">-ApiVersion</span></span>
<span data-ttu-id="8298f-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8298f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8298f-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="8298f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8298f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8298f-119">-DefaultProfile</span></span>
<span data-ttu-id="8298f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8298f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8298f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="8298f-121">-Id</span></span>
<span data-ttu-id="8298f-122">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="8298f-122">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="8298f-123">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="8298f-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8298f-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8298f-124">-Name</span></span>
<span data-ttu-id="8298f-125">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8298f-125">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8298f-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="8298f-126">-Pre</span></span>
<span data-ttu-id="8298f-127">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="8298f-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8298f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8298f-128">-ResourceGroupName</span></span>
<span data-ttu-id="8298f-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8298f-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8298f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8298f-130">CommonParameters</span></span>
<span data-ttu-id="8298f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8298f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8298f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8298f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8298f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8298f-133">INPUTS</span></span>

### <span data-ttu-id="8298f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8298f-134">System.String</span></span>

## <span data-ttu-id="8298f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8298f-135">OUTPUTS</span></span>

### <span data-ttu-id="8298f-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8298f-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8298f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8298f-137">NOTES</span></span>

## <span data-ttu-id="8298f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8298f-138">RELATED LINKS</span></span>

