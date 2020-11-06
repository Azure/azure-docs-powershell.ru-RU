---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: c74f4f89337d8fee4e6739cb145e9d2da0d4b81c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559731"
---
# <span data-ttu-id="f6a9b-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f6a9b-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="f6a9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a9b-103">Получение партнеров по учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6a9b-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a9b-106">Командлет **Get-AzureRmIntegrationAccountPartner** получает партнеров учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="f6a9b-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="f6a9b-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f6a9b-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f6a9b-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f6a9b-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f6a9b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-112">EXAMPLES</span></span>

### <span data-ttu-id="f6a9b-113">Пример 1: получение партнера учетной записи для интеграции</span><span class="sxs-lookup"><span data-stu-id="f6a9b-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="f6a9b-114">Эта команда получает партнера учетной записи интеграции с именем IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="f6a9b-115">Пример 2: получение партнеров по учетной записи интеграции с помощью имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="f6a9b-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="f6a9b-116">Эта команда получает партнеров учетной записи интеграции для учетной записи интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="f6a9b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-117">PARAMETERS</span></span>

### <span data-ttu-id="f6a9b-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6a9b-118">-Name</span></span>
<span data-ttu-id="f6a9b-119">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f6a9b-120">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="f6a9b-120">-PartnerName</span></span>
<span data-ttu-id="f6a9b-121">Указывает имя партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-121">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="f6a9b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a9b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6a9b-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f6a9b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a9b-124">-DefaultProfile</span></span>
<span data-ttu-id="f6a9b-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a9b-126">CommonParameters</span></span>
<span data-ttu-id="f6a9b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a9b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a9b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a9b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6a9b-129">INPUTS</span></span>

## <span data-ttu-id="f6a9b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-130">OUTPUTS</span></span>

### <span data-ttu-id="f6a9b-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f6a9b-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="f6a9b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6a9b-132">NOTES</span></span>

## <span data-ttu-id="f6a9b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-133">RELATED LINKS</span></span>

[<span data-ttu-id="f6a9b-134">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f6a9b-134">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="f6a9b-135">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f6a9b-135">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="f6a9b-136">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f6a9b-136">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


