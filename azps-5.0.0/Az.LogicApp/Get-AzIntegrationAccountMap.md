---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 99f6bcda0360395826dedc02e3d8b968ee23795d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250169"
---
# <span data-ttu-id="a37c2-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a37c2-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="a37c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a37c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a37c2-103">Возвращает карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a37c2-103">Gets an integration account map.</span></span>

## <span data-ttu-id="a37c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a37c2-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a37c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a37c2-105">DESCRIPTION</span></span>
<span data-ttu-id="a37c2-106">Командлет **Get-AzIntegrationAccountMap** получает карту учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a37c2-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="a37c2-107">Указание имени учетной записи интеграции, имени группы ресурсов и имени карты.</span><span class="sxs-lookup"><span data-stu-id="a37c2-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="a37c2-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a37c2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a37c2-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="a37c2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a37c2-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="a37c2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a37c2-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="a37c2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a37c2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a37c2-112">EXAMPLES</span></span>

### <span data-ttu-id="a37c2-113">Пример 1: получение карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="a37c2-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="a37c2-114">Эта команда получает карту учетной записи интеграции с именем IntegrationAccountMap47 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a37c2-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="a37c2-115">Пример 2: получение карт учетной записи интеграции по имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="a37c2-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="a37c2-116">Эта команда получает сопоставления учетной записи интеграции с именем учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a37c2-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="a37c2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a37c2-117">PARAMETERS</span></span>

### <span data-ttu-id="a37c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37c2-118">-DefaultProfile</span></span>
<span data-ttu-id="a37c2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a37c2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a37c2-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="a37c2-120">-MapName</span></span>
<span data-ttu-id="a37c2-121">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a37c2-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="a37c2-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="a37c2-122">-MapType</span></span>
<span data-ttu-id="a37c2-123">Тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a37c2-123">The integration account map type.</span></span>

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

### <span data-ttu-id="a37c2-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a37c2-124">-Name</span></span>
<span data-ttu-id="a37c2-125">Указывает имя для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a37c2-125">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="a37c2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a37c2-126">-ResourceGroupName</span></span>
<span data-ttu-id="a37c2-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a37c2-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a37c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37c2-128">CommonParameters</span></span>
<span data-ttu-id="a37c2-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a37c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a37c2-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a37c2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37c2-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a37c2-131">INPUTS</span></span>

### <span data-ttu-id="a37c2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a37c2-132">System.String</span></span>

## <span data-ttu-id="a37c2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a37c2-133">OUTPUTS</span></span>

### <span data-ttu-id="a37c2-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a37c2-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="a37c2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a37c2-135">NOTES</span></span>

## <span data-ttu-id="a37c2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a37c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="a37c2-137">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a37c2-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="a37c2-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a37c2-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="a37c2-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a37c2-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


