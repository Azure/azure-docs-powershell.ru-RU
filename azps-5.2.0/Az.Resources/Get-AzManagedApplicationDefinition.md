---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325279"
---
# <span data-ttu-id="06dfd-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="06dfd-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="06dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="06dfd-103">Получает определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="06dfd-103">Gets managed application definitions</span></span>

## <span data-ttu-id="06dfd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06dfd-104">SYNTAX</span></span>

### <span data-ttu-id="06dfd-105">GetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06dfd-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06dfd-106">GetById</span><span class="sxs-lookup"><span data-stu-id="06dfd-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06dfd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06dfd-107">DESCRIPTION</span></span>
<span data-ttu-id="06dfd-108">Cmdlet **Get-AzManagedApplicationDefinition** получает определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="06dfd-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="06dfd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06dfd-109">EXAMPLES</span></span>

### <span data-ttu-id="06dfd-110">Пример 1. Получение всех определений управляемых приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="06dfd-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="06dfd-111">Эта команда получает определения управляемых приложений в группе ресурсов MyRG.</span><span class="sxs-lookup"><span data-stu-id="06dfd-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="06dfd-112">Пример 2. Получение определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="06dfd-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="06dfd-113">Эта команда получает определение управляемого приложения "myManagedAppDef" в группе ресурсов "MyRG"</span><span class="sxs-lookup"><span data-stu-id="06dfd-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="06dfd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06dfd-114">PARAMETERS</span></span>

### <span data-ttu-id="06dfd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06dfd-115">-ApiVersion</span></span>
<span data-ttu-id="06dfd-116">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06dfd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="06dfd-117">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="06dfd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="06dfd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06dfd-118">-DefaultProfile</span></span>
<span data-ttu-id="06dfd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06dfd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06dfd-120">-Id</span><span class="sxs-lookup"><span data-stu-id="06dfd-120">-Id</span></span>
<span data-ttu-id="06dfd-121">Полное определение приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="06dfd-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="06dfd-122">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="06dfd-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06dfd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="06dfd-123">-Name</span></span>
<span data-ttu-id="06dfd-124">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="06dfd-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06dfd-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="06dfd-125">-Pre</span></span>
<span data-ttu-id="06dfd-126">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="06dfd-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="06dfd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06dfd-127">-ResourceGroupName</span></span>
<span data-ttu-id="06dfd-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06dfd-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06dfd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dfd-129">CommonParameters</span></span>
<span data-ttu-id="06dfd-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06dfd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dfd-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06dfd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dfd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06dfd-132">INPUTS</span></span>

### <span data-ttu-id="06dfd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="06dfd-133">System.String</span></span>

## <span data-ttu-id="06dfd-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06dfd-134">OUTPUTS</span></span>

### <span data-ttu-id="06dfd-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="06dfd-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06dfd-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06dfd-136">NOTES</span></span>

## <span data-ttu-id="06dfd-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06dfd-137">RELATED LINKS</span></span>
