---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: e854d9e77ba72ca297b2b9ca9a8d20f55d6194fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900001"
---
# <span data-ttu-id="97956-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="97956-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="97956-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97956-102">SYNOPSIS</span></span>
<span data-ttu-id="97956-103">Получает сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="97956-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="97956-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97956-104">SYNTAX</span></span>

### <span data-ttu-id="97956-105">ByIntegrationAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97956-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97956-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="97956-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97956-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97956-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97956-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97956-108">DESCRIPTION</span></span>
<span data-ttu-id="97956-109">Командлет **Get-AzIntegrationAccountAssembly** получает сборку из учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="97956-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="97956-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97956-110">EXAMPLES</span></span>

### <span data-ttu-id="97956-111">Пример 1: получение сборки с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="97956-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="97956-112">Получить сборку с именем "sampleAssembly", расположенную в учетной записи интеграции "sampleIntegrationAccount", которая содержится в группе ресурсов "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="97956-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="97956-113">Пример 2: список всех сборок в учетной записи интеграции с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="97956-113">Example 2: List all assemblies in an integration account by parameters</span></span>
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

<span data-ttu-id="97956-114">Получение всех сборок, расположенных в учетной записи интеграции "sampleIntegrationAccount", которая содержится в группе ресурсов "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="97956-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="97956-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97956-115">PARAMETERS</span></span>

### <span data-ttu-id="97956-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97956-116">-DefaultProfile</span></span>
<span data-ttu-id="97956-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97956-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97956-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97956-118">-Name</span></span>
<span data-ttu-id="97956-119">Имя сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="97956-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="97956-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="97956-120">-ParentName</span></span>
<span data-ttu-id="97956-121">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="97956-121">The integration account name.</span></span>

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

### <span data-ttu-id="97956-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="97956-122">-ParentObject</span></span>
<span data-ttu-id="97956-123">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="97956-123">An integration account object.</span></span>

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

### <span data-ttu-id="97956-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="97956-124">-ParentResourceId</span></span>
<span data-ttu-id="97956-125">Идентификатор ресурса для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="97956-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="97956-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97956-126">-ResourceGroupName</span></span>
<span data-ttu-id="97956-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97956-127">The resource group name.</span></span>

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

### <span data-ttu-id="97956-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97956-128">CommonParameters</span></span>
<span data-ttu-id="97956-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97956-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97956-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97956-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97956-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97956-131">INPUTS</span></span>

### <span data-ttu-id="97956-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="97956-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="97956-133">System. String</span><span class="sxs-lookup"><span data-stu-id="97956-133">System.String</span></span>

## <span data-ttu-id="97956-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97956-134">OUTPUTS</span></span>

### <span data-ttu-id="97956-135">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="97956-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="97956-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="97956-136">NOTES</span></span>

## <span data-ttu-id="97956-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97956-137">RELATED LINKS</span></span>
