---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: c5bbefe1edc36d63dcac53ad85923da3f75d80e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566772"
---
# <span data-ttu-id="b856f-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="b856f-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="b856f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b856f-102">SYNOPSIS</span></span>
<span data-ttu-id="b856f-103">Получение определений управляемых приложений</span><span class="sxs-lookup"><span data-stu-id="b856f-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b856f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b856f-104">SYNTAX</span></span>

### <span data-ttu-id="b856f-105">GetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b856f-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b856f-106">GetById</span><span class="sxs-lookup"><span data-stu-id="b856f-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b856f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b856f-107">DESCRIPTION</span></span>
<span data-ttu-id="b856f-108">Командлет **Get-AzureRmManagedApplicationDefinition** получает определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="b856f-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="b856f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b856f-109">EXAMPLES</span></span>

### <span data-ttu-id="b856f-110">Пример 1: получение всех определений управляемых приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b856f-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="b856f-111">Эта команда получает определения управляемых приложений в группе ресурсов "MyRG".</span><span class="sxs-lookup"><span data-stu-id="b856f-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="b856f-112">Пример 2: получение определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="b856f-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="b856f-113">Эта команда получает определение управляемого приложения "myManagedAppDef" в разделе "Группа ресурсов" MyRG "</span><span class="sxs-lookup"><span data-stu-id="b856f-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="b856f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b856f-114">PARAMETERS</span></span>

### <span data-ttu-id="b856f-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b856f-115">-ApiVersion</span></span>
<span data-ttu-id="b856f-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b856f-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b856f-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="b856f-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b856f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b856f-118">-DefaultProfile</span></span>
<span data-ttu-id="b856f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b856f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b856f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="b856f-120">-Id</span></span>
<span data-ttu-id="b856f-121">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="b856f-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="b856f-122">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b856f-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b856f-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b856f-123">-Name</span></span>
<span data-ttu-id="b856f-124">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b856f-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="b856f-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="b856f-125">-Pre</span></span>
<span data-ttu-id="b856f-126">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="b856f-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b856f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b856f-127">-ResourceGroupName</span></span>
<span data-ttu-id="b856f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b856f-128">The resource group name.</span></span>

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

### <span data-ttu-id="b856f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b856f-129">CommonParameters</span></span>
<span data-ttu-id="b856f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b856f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b856f-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b856f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b856f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b856f-132">INPUTS</span></span>

### <span data-ttu-id="b856f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b856f-133">System.String</span></span>

## <span data-ttu-id="b856f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b856f-134">OUTPUTS</span></span>

### <span data-ttu-id="b856f-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b856f-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b856f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b856f-136">NOTES</span></span>

## <span data-ttu-id="b856f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b856f-137">RELATED LINKS</span></span>
