---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 340320ee102317069e81806ba9a7831dc1077368
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566983"
---
# <span data-ttu-id="0b2f5-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b2f5-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="0b2f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b2f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2f5-103">Возвращает карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b2f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b2f5-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b2f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b2f5-105">DESCRIPTION</span></span>
<span data-ttu-id="0b2f5-106">Командлет **Get-AzureRmIntegrationAccountMap** получает карту учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="0b2f5-107">Указание имени учетной записи интеграции, имени группы ресурсов и имени карты.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-107">Specifying the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="0b2f5-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0b2f5-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0b2f5-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0b2f5-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0b2f5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b2f5-112">EXAMPLES</span></span>

### <span data-ttu-id="0b2f5-113">Пример 1: получение карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="0b2f5-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="0b2f5-114">Эта команда получает карту учетной записи интеграции с именем IntegrationAccountMap47 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="0b2f5-115">Пример 2: получение карт учетной записи интеграции по имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="0b2f5-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="0b2f5-116">Эта команда получает сопоставления учетной записи интеграции с именем учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="0b2f5-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b2f5-117">PARAMETERS</span></span>

### <span data-ttu-id="0b2f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2f5-118">-DefaultProfile</span></span>
<span data-ttu-id="0b2f5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0b2f5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b2f5-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="0b2f5-120">-MapName</span></span>
<span data-ttu-id="0b2f5-121">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="0b2f5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b2f5-122">-Name</span></span>
<span data-ttu-id="0b2f5-123">Указывает имя для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-123">Specifies the name for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2f5-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b2f5-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2f5-126">CommonParameters</span></span>
<span data-ttu-id="0b2f5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2f5-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2f5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2f5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b2f5-129">INPUTS</span></span>

### <span data-ttu-id="0b2f5-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="0b2f5-130">None</span></span>
<span data-ttu-id="0b2f5-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0b2f5-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b2f5-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b2f5-132">OUTPUTS</span></span>

### <span data-ttu-id="0b2f5-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b2f5-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="0b2f5-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b2f5-134">NOTES</span></span>

## <span data-ttu-id="0b2f5-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b2f5-135">RELATED LINKS</span></span>

[<span data-ttu-id="0b2f5-136">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b2f5-136">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="0b2f5-137">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b2f5-137">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="0b2f5-138">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b2f5-138">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


