---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237529"
---
# <span data-ttu-id="bcc48-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcc48-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="bcc48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcc48-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc48-103">Получает пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bcc48-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="bcc48-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcc48-104">SYNTAX</span></span>

### <span data-ttu-id="bcc48-105">ByIntegrationAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bcc48-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc48-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bcc48-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc48-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bcc48-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcc48-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcc48-108">DESCRIPTION</span></span>
<span data-ttu-id="bcc48-109">Для получения пакетной конфигурации из учетной записи интеграции получается **cmdlet Get-AzIntegrationAccountBatchConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="bcc48-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="bcc48-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcc48-110">EXAMPLES</span></span>

### <span data-ttu-id="bcc48-111">Пример 1. Настройка пакета по параметрам</span><span class="sxs-lookup"><span data-stu-id="bcc48-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="bcc48-112">Получите пакетную конфигурацию sampleBatchConfig, расположенную в учетной записи интеграции sampleIntegrationAccount, которая находится в группе ресурсов "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="bcc48-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="bcc48-113">Пример 2. Список всех пакетных конфигураций в учетной записи интеграции по параметрам</span><span class="sxs-lookup"><span data-stu-id="bcc48-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="bcc48-114">Все пакетные конфигурации находятся в учетной записи интеграции sampleIntegrationAccount, которая содержится в группе ресурсов sampleResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bcc48-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="bcc48-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcc48-115">PARAMETERS</span></span>

### <span data-ttu-id="bcc48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc48-116">-DefaultProfile</span></span>
<span data-ttu-id="bcc48-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc48-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bcc48-118">-Name</span></span>
<span data-ttu-id="bcc48-119">Имя пакета конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bcc48-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc48-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="bcc48-120">-ParentName</span></span>
<span data-ttu-id="bcc48-121">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bcc48-121">The integration account name.</span></span>

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

### <span data-ttu-id="bcc48-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bcc48-122">-ParentObject</span></span>
<span data-ttu-id="bcc48-123">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bcc48-123">An integration account object.</span></span>

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

### <span data-ttu-id="bcc48-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bcc48-124">-ParentResourceId</span></span>
<span data-ttu-id="bcc48-125">ИД ресурса учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="bcc48-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="bcc48-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc48-126">-ResourceGroupName</span></span>
<span data-ttu-id="bcc48-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bcc48-127">The resource group name.</span></span>

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

### <span data-ttu-id="bcc48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc48-128">CommonParameters</span></span>
<span data-ttu-id="bcc48-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc48-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc48-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc48-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcc48-131">INPUTS</span></span>

### <span data-ttu-id="bcc48-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="bcc48-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="bcc48-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bcc48-133">System.String</span></span>

## <span data-ttu-id="bcc48-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcc48-134">OUTPUTS</span></span>

### <span data-ttu-id="bcc48-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcc48-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="bcc48-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcc48-136">NOTES</span></span>

## <span data-ttu-id="bcc48-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcc48-137">RELATED LINKS</span></span>
