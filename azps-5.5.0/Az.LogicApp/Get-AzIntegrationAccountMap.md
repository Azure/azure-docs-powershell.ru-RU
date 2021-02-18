---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 99f6bcda0360395826dedc02e3d8b968ee23795d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228324"
---
# <span data-ttu-id="463f5-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="463f5-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="463f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="463f5-102">SYNOPSIS</span></span>
<span data-ttu-id="463f5-103">Возвращает интеграцию с картой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="463f5-103">Gets an integration account map.</span></span>

## <span data-ttu-id="463f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="463f5-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="463f5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="463f5-105">DESCRIPTION</span></span>
<span data-ttu-id="463f5-106">Для интеграции с группой ресурсов возвращается карта учетной записи **Get-AzIntegrationAccountMap.**</span><span class="sxs-lookup"><span data-stu-id="463f5-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="463f5-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="463f5-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="463f5-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="463f5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="463f5-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="463f5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="463f5-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="463f5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="463f5-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="463f5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="463f5-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="463f5-112">EXAMPLES</span></span>

### <span data-ttu-id="463f5-113">Пример 1. Получить интеграцию с картой учетной записи</span><span class="sxs-lookup"><span data-stu-id="463f5-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
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

<span data-ttu-id="463f5-114">Эта команда получает интеграцию с именем IntegrationAccountMap47 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="463f5-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="463f5-115">Пример 2. Интеграция карт учетной записи по имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="463f5-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="463f5-116">Эта команда получает карты учетной записи интеграции по имени учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="463f5-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="463f5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="463f5-117">PARAMETERS</span></span>

### <span data-ttu-id="463f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463f5-118">-DefaultProfile</span></span>
<span data-ttu-id="463f5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="463f5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="463f5-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="463f5-120">-MapName</span></span>
<span data-ttu-id="463f5-121">Указывает имя интеграционной карты учетной записи.</span><span class="sxs-lookup"><span data-stu-id="463f5-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="463f5-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="463f5-122">-MapType</span></span>
<span data-ttu-id="463f5-123">Тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="463f5-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463f5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="463f5-124">-Name</span></span>
<span data-ttu-id="463f5-125">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="463f5-125">Specifies the name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463f5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463f5-126">-ResourceGroupName</span></span>
<span data-ttu-id="463f5-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="463f5-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="463f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463f5-128">CommonParameters</span></span>
<span data-ttu-id="463f5-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463f5-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463f5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463f5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="463f5-131">INPUTS</span></span>

### <span data-ttu-id="463f5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="463f5-132">System.String</span></span>

## <span data-ttu-id="463f5-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="463f5-133">OUTPUTS</span></span>

### <span data-ttu-id="463f5-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="463f5-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="463f5-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="463f5-135">NOTES</span></span>

## <span data-ttu-id="463f5-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="463f5-136">RELATED LINKS</span></span>

[<span data-ttu-id="463f5-137">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="463f5-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="463f5-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="463f5-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="463f5-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="463f5-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


