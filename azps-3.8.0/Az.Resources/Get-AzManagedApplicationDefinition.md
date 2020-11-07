---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912624"
---
# <span data-ttu-id="4a538-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="4a538-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="4a538-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a538-102">SYNOPSIS</span></span>
<span data-ttu-id="4a538-103">Получение определений управляемых приложений</span><span class="sxs-lookup"><span data-stu-id="4a538-103">Gets managed application definitions</span></span>

## <span data-ttu-id="4a538-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a538-104">SYNTAX</span></span>

### <span data-ttu-id="4a538-105">GetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a538-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a538-106">GetById</span><span class="sxs-lookup"><span data-stu-id="4a538-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a538-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a538-107">DESCRIPTION</span></span>
<span data-ttu-id="4a538-108">Командлет **Get-AzManagedApplicationDefinition** получает определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="4a538-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="4a538-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a538-109">EXAMPLES</span></span>

### <span data-ttu-id="4a538-110">Пример 1: получение всех определений управляемых приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="4a538-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="4a538-111">Эта команда получает определения управляемых приложений в группе ресурсов "MyRG".</span><span class="sxs-lookup"><span data-stu-id="4a538-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="4a538-112">Пример 2: получение определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="4a538-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="4a538-113">Эта команда получает определение управляемого приложения "myManagedAppDef" в разделе "Группа ресурсов" MyRG "</span><span class="sxs-lookup"><span data-stu-id="4a538-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="4a538-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a538-114">PARAMETERS</span></span>

### <span data-ttu-id="4a538-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4a538-115">-ApiVersion</span></span>
<span data-ttu-id="4a538-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a538-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4a538-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="4a538-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4a538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a538-118">-DefaultProfile</span></span>
<span data-ttu-id="4a538-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a538-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a538-120">-ID</span><span class="sxs-lookup"><span data-stu-id="4a538-120">-Id</span></span>
<span data-ttu-id="4a538-121">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="4a538-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="4a538-122">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="4a538-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="4a538-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a538-123">-Name</span></span>
<span data-ttu-id="4a538-124">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="4a538-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="4a538-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="4a538-125">-Pre</span></span>
<span data-ttu-id="4a538-126">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="4a538-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4a538-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a538-127">-ResourceGroupName</span></span>
<span data-ttu-id="4a538-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a538-128">The resource group name.</span></span>

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

### <span data-ttu-id="4a538-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a538-129">CommonParameters</span></span>
<span data-ttu-id="4a538-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a538-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a538-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a538-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a538-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a538-132">INPUTS</span></span>

### <span data-ttu-id="4a538-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4a538-133">System.String</span></span>

## <span data-ttu-id="4a538-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a538-134">OUTPUTS</span></span>

### <span data-ttu-id="4a538-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4a538-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4a538-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a538-136">NOTES</span></span>

## <span data-ttu-id="4a538-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a538-137">RELATED LINKS</span></span>
