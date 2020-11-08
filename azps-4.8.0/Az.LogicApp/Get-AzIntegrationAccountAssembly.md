---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236311"
---
# <span data-ttu-id="a239d-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a239d-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="a239d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a239d-102">SYNOPSIS</span></span>
<span data-ttu-id="a239d-103">Получает сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a239d-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="a239d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a239d-104">SYNTAX</span></span>

### <span data-ttu-id="a239d-105">ByIntegrationAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a239d-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a239d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a239d-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a239d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a239d-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a239d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a239d-108">DESCRIPTION</span></span>
<span data-ttu-id="a239d-109">Командлет **Get-AzIntegrationAccountAssembly** получает сборку из учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a239d-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="a239d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a239d-110">EXAMPLES</span></span>

### <span data-ttu-id="a239d-111">Пример 1: получение сборки с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="a239d-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a239d-112">Получить сборку с именем "sampleAssembly", расположенную в учетной записи интеграции "sampleIntegrationAccount", которая содержится в группе ресурсов "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="a239d-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="a239d-113">Пример 2: список всех сборок в учетной записи интеграции с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="a239d-113">Example 2: List all assemblies in an integration account by parameters</span></span>
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

<span data-ttu-id="a239d-114">Получение всех сборок, расположенных в учетной записи интеграции "sampleIntegrationAccount", которая содержится в группе ресурсов "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="a239d-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="a239d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a239d-115">PARAMETERS</span></span>

### <span data-ttu-id="a239d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a239d-116">-DefaultProfile</span></span>
<span data-ttu-id="a239d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a239d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a239d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a239d-118">-Name</span></span>
<span data-ttu-id="a239d-119">Имя сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a239d-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="a239d-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="a239d-120">-ParentName</span></span>
<span data-ttu-id="a239d-121">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a239d-121">The integration account name.</span></span>

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

### <span data-ttu-id="a239d-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a239d-122">-ParentObject</span></span>
<span data-ttu-id="a239d-123">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a239d-123">An integration account object.</span></span>

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

### <span data-ttu-id="a239d-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a239d-124">-ParentResourceId</span></span>
<span data-ttu-id="a239d-125">Идентификатор ресурса для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a239d-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="a239d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a239d-126">-ResourceGroupName</span></span>
<span data-ttu-id="a239d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a239d-127">The resource group name.</span></span>

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

### <span data-ttu-id="a239d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a239d-128">CommonParameters</span></span>
<span data-ttu-id="a239d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a239d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a239d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a239d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a239d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a239d-131">INPUTS</span></span>

### <span data-ttu-id="a239d-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="a239d-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="a239d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a239d-133">System.String</span></span>

## <span data-ttu-id="a239d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a239d-134">OUTPUTS</span></span>

### <span data-ttu-id="a239d-135">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a239d-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="a239d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a239d-136">NOTES</span></span>

## <span data-ttu-id="a239d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a239d-137">RELATED LINKS</span></span>
