---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 46cc7c75075cffface03af2ed70b5339dd36b0a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226385"
---
# <span data-ttu-id="6541d-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6541d-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="6541d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6541d-102">SYNOPSIS</span></span>
<span data-ttu-id="6541d-103">Получает соглашение об интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="6541d-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="6541d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6541d-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6541d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6541d-105">DESCRIPTION</span></span>
<span data-ttu-id="6541d-106">Для получения соглашения об учетной записи **Get-AzIntegrationAccountAgreement** от группы ресурсов Azure требуется соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6541d-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="6541d-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя соглашения.</span><span class="sxs-lookup"><span data-stu-id="6541d-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="6541d-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="6541d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6541d-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="6541d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6541d-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="6541d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6541d-111">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="6541d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6541d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6541d-112">EXAMPLES</span></span>

### <span data-ttu-id="6541d-113">Пример 1. Получить соглашение об интеграции с учетной записью</span><span class="sxs-lookup"><span data-stu-id="6541d-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="6541d-114">Эта команда получает соглашение об интеграции с учетной записью IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="6541d-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="6541d-115">Пример 2. Соглашения об интеграции с учетной записью по имени группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6541d-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="6541d-116">Эта команда получает соглашения об интеграции с учетной записью по имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6541d-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="6541d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6541d-117">PARAMETERS</span></span>

### <span data-ttu-id="6541d-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="6541d-118">-AgreementName</span></span>
<span data-ttu-id="6541d-119">Указывает имя соглашения об интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="6541d-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="6541d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6541d-120">-DefaultProfile</span></span>
<span data-ttu-id="6541d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6541d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6541d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6541d-122">-Name</span></span>
<span data-ttu-id="6541d-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6541d-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="6541d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6541d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6541d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6541d-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6541d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6541d-126">CommonParameters</span></span>
<span data-ttu-id="6541d-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6541d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6541d-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6541d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6541d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6541d-129">INPUTS</span></span>

### <span data-ttu-id="6541d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6541d-130">System.String</span></span>

## <span data-ttu-id="6541d-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6541d-131">OUTPUTS</span></span>

### <span data-ttu-id="6541d-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountagreement</span><span class="sxs-lookup"><span data-stu-id="6541d-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="6541d-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6541d-133">NOTES</span></span>

## <span data-ttu-id="6541d-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6541d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6541d-135">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6541d-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="6541d-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6541d-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="6541d-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6541d-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


