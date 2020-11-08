---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079575"
---
# <span data-ttu-id="30142-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="30142-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="30142-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30142-102">SYNOPSIS</span></span>
<span data-ttu-id="30142-103">Создание соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="30142-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30142-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30142-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30142-105">DESCRIPTION</span></span>
<span data-ttu-id="30142-106">Командлет **New-AzIntegrationAccountAgreement** создает соглашение с учетной записью интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="30142-107">Этот командлет возвращает объект, представляющий соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="30142-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя соглашения, тип, имя партнера, классификаторы партнеров и содержимое соглашения.</span><span class="sxs-lookup"><span data-stu-id="30142-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="30142-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="30142-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="30142-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="30142-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="30142-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="30142-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="30142-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="30142-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="30142-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="30142-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="30142-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30142-114">EXAMPLES</span></span>

### <span data-ttu-id="30142-115">Пример 1: создание соглашения для учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="30142-115">Example 1: Create a integration account agreement</span></span>
```powershell
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="30142-116">Эта команда создает соглашение с учетной записью интеграции в указанной группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="30142-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="30142-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="30142-117">Example 2</span></span>

<span data-ttu-id="30142-118">Создание соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-118">Creates an integration account agreement.</span></span> <span data-ttu-id="30142-119">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="30142-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="30142-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30142-120">PARAMETERS</span></span>

### <span data-ttu-id="30142-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="30142-121">-AgreementContent</span></span>
<span data-ttu-id="30142-122">Определяет содержимое соглашения в формате JavaScript Object Notation (JSON) для соглашения.</span><span class="sxs-lookup"><span data-stu-id="30142-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="30142-123">Укажите либо этот параметр, либо параметр *AgreementContentFilePath* .</span><span class="sxs-lookup"><span data-stu-id="30142-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="30142-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="30142-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="30142-125">Задает путь к файлу соглашения для соглашения.</span><span class="sxs-lookup"><span data-stu-id="30142-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="30142-126">Укажите либо этот параметр, либо параметр *AgreementContent* .</span><span class="sxs-lookup"><span data-stu-id="30142-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="30142-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="30142-127">-AgreementName</span></span>
<span data-ttu-id="30142-128">Указывает имя для соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-128">Specifies a name for the integration account agreement.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30142-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="30142-129">-AgreementType</span></span>
<span data-ttu-id="30142-130">Указывает тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="30142-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="30142-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30142-132">X12</span><span class="sxs-lookup"><span data-stu-id="30142-132">X12</span></span> 
- <span data-ttu-id="30142-133">AS2</span><span class="sxs-lookup"><span data-stu-id="30142-133">AS2</span></span>
- <span data-ttu-id="30142-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="30142-134">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30142-135">-DefaultProfile</span></span>
<span data-ttu-id="30142-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="30142-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30142-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="30142-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="30142-138">Указывает идентификационный ограничитель имени для гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="30142-138">Specifies a name business identity qualifier for the guest partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="30142-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="30142-140">Значение описателя идентификации гостя для соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-140">The integration account agreement guest identity qualifier value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="30142-141">-GuestPartner</span></span>
<span data-ttu-id="30142-142">Указывает имя гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="30142-142">Specifies the name of the guest partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="30142-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="30142-144">Указывает классификатор имени бизнес-удостоверения для партнера узла.</span><span class="sxs-lookup"><span data-stu-id="30142-144">Specifies a name business identity qualifier for the host partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="30142-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="30142-146">Значение описателя идентификатора узла для соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-146">The integration account agreement host identity qualifier value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="30142-147">-HostPartner</span></span>
<span data-ttu-id="30142-148">Указывает имя партнера узла.</span><span class="sxs-lookup"><span data-stu-id="30142-148">Specifies the name of the host partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="30142-149">-Metadata</span></span>
<span data-ttu-id="30142-150">Указывает объект метаданных для соглашения.</span><span class="sxs-lookup"><span data-stu-id="30142-150">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-151">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30142-151">-Name</span></span>
<span data-ttu-id="30142-152">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="30142-152">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30142-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30142-153">-ResourceGroupName</span></span>
<span data-ttu-id="30142-154">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30142-154">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30142-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30142-155">-Confirm</span></span>
<span data-ttu-id="30142-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30142-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30142-157">-WhatIf</span></span>
<span data-ttu-id="30142-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30142-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30142-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30142-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30142-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30142-160">CommonParameters</span></span>
<span data-ttu-id="30142-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30142-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30142-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30142-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30142-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30142-163">INPUTS</span></span>

### <span data-ttu-id="30142-164">System. String</span><span class="sxs-lookup"><span data-stu-id="30142-164">System.String</span></span>

## <span data-ttu-id="30142-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30142-165">OUTPUTS</span></span>

### <span data-ttu-id="30142-166">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="30142-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="30142-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="30142-167">NOTES</span></span>

## <span data-ttu-id="30142-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30142-168">RELATED LINKS</span></span>

[<span data-ttu-id="30142-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="30142-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="30142-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="30142-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="30142-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="30142-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


