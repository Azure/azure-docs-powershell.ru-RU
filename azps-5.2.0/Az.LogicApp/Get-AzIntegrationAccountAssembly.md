---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400836"
---
# <span data-ttu-id="d66dd-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d66dd-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d66dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d66dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d66dd-103">Получает сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66dd-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="d66dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d66dd-104">SYNTAX</span></span>

### <span data-ttu-id="d66dd-105">ByIntegrationAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d66dd-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d66dd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d66dd-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d66dd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d66dd-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d66dd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d66dd-108">DESCRIPTION</span></span>
<span data-ttu-id="d66dd-109">Cmdlet **Get-AzIntegrationAccountAssembly** получает сборку из учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66dd-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="d66dd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d66dd-110">EXAMPLES</span></span>

### <span data-ttu-id="d66dd-111">Пример 1. Сборка по параметрам</span><span class="sxs-lookup"><span data-stu-id="d66dd-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d66dd-112">Получите сборку sampleAssembly, расположенную в учетной записи интеграции sampleIntegrationAccount, которая содержится в группе ресурсов "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d66dd-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="d66dd-113">Пример 2. Со списком всех сборок в учетной записи интеграции по параметрам</span><span class="sxs-lookup"><span data-stu-id="d66dd-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d66dd-114">Получите все сборки из учетной записи интеграции sampleIntegrationAccount, которая содержится в группе ресурсов SampleResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d66dd-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="d66dd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d66dd-115">PARAMETERS</span></span>

### <span data-ttu-id="d66dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66dd-116">-DefaultProfile</span></span>
<span data-ttu-id="d66dd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d66dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66dd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d66dd-118">-Name</span></span>
<span data-ttu-id="d66dd-119">Имя сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66dd-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="d66dd-120">-ParentName</span></span>
<span data-ttu-id="d66dd-121">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66dd-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d66dd-122">-ParentObject</span></span>
<span data-ttu-id="d66dd-123">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66dd-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d66dd-124">-ParentResourceId</span></span>
<span data-ttu-id="d66dd-125">ИД ресурса учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66dd-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66dd-126">-ResourceGroupName</span></span>
<span data-ttu-id="d66dd-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d66dd-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66dd-128">CommonParameters</span></span>
<span data-ttu-id="d66dd-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d66dd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66dd-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d66dd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66dd-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d66dd-131">INPUTS</span></span>

### <span data-ttu-id="d66dd-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d66dd-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="d66dd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d66dd-133">System.String</span></span>

## <span data-ttu-id="d66dd-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d66dd-134">OUTPUTS</span></span>

### <span data-ttu-id="d66dd-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d66dd-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d66dd-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d66dd-136">NOTES</span></span>

## <span data-ttu-id="d66dd-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d66dd-137">RELATED LINKS</span></span>