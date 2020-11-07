---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: eadd3052bb965b60bdaf377cd45fc014f25cac79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733273"
---
# <span data-ttu-id="40f5f-101">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="40f5f-101">Get-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="40f5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="40f5f-103">Получает соглашение о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="40f5f-103">Gets an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40f5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40f5f-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40f5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="40f5f-106">Командлет **Get-AzureRmIntegrationAccountAgreement** получает соглашение о учетной записи интеграции из группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="40f5f-106">The **Get-AzureRmIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="40f5f-107">Укажите имя учетной записи интеграции, имя группы ресурсов и название соглашения.</span><span class="sxs-lookup"><span data-stu-id="40f5f-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="40f5f-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="40f5f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="40f5f-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="40f5f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="40f5f-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="40f5f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="40f5f-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="40f5f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="40f5f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40f5f-112">EXAMPLES</span></span>

### <span data-ttu-id="40f5f-113">Пример 1: получение соглашения о учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="40f5f-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
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

<span data-ttu-id="40f5f-114">Эта команда получает соглашение о учетной записи интеграции с именем IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="40f5f-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="40f5f-115">Пример 2: получение соглашений о учетной записи интеграции по названию группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="40f5f-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="40f5f-116">Эта команда получает соглашения учетной записи интеграции по имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40f5f-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="40f5f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40f5f-117">PARAMETERS</span></span>

### <span data-ttu-id="40f5f-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="40f5f-118">-AgreementName</span></span>
<span data-ttu-id="40f5f-119">Указывает имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="40f5f-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="40f5f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f5f-120">-DefaultProfile</span></span>
<span data-ttu-id="40f5f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="40f5f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40f5f-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40f5f-122">-Name</span></span>
<span data-ttu-id="40f5f-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="40f5f-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="40f5f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f5f-124">-ResourceGroupName</span></span>
<span data-ttu-id="40f5f-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40f5f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="40f5f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f5f-126">CommonParameters</span></span>
<span data-ttu-id="40f5f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40f5f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f5f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40f5f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f5f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40f5f-129">INPUTS</span></span>

### <span data-ttu-id="40f5f-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="40f5f-130">None</span></span>
<span data-ttu-id="40f5f-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="40f5f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40f5f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40f5f-132">OUTPUTS</span></span>

### <span data-ttu-id="40f5f-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="40f5f-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="40f5f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="40f5f-134">NOTES</span></span>

## <span data-ttu-id="40f5f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40f5f-135">RELATED LINKS</span></span>

[<span data-ttu-id="40f5f-136">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="40f5f-136">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="40f5f-137">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="40f5f-137">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="40f5f-138">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="40f5f-138">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


