---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 10cd1993acccf45e39a1b192f44b715b06f6d1d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720525"
---
# <span data-ttu-id="cd6cf-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cd6cf-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="cd6cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6cf-103">Создание соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="cd6cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd6cf-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd6cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd6cf-105">DESCRIPTION</span></span>
<span data-ttu-id="cd6cf-106">Командлет **New-AzIntegrationAccountAgreement** создает соглашение с учетной записью интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="cd6cf-107">Этот командлет возвращает объект, представляющий соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="cd6cf-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя соглашения, тип, имя партнера, классификаторы партнеров и содержимое соглашения.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="cd6cf-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="cd6cf-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cd6cf-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cd6cf-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cd6cf-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cd6cf-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd6cf-114">EXAMPLES</span></span>

### <span data-ttu-id="cd6cf-115">Пример 1: создание соглашения для учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="cd6cf-115">Example 1: Create a integration account agreement</span></span>
```
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

<span data-ttu-id="cd6cf-116">Эта команда создает соглашение с учетной записью интеграции в указанной группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="cd6cf-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd6cf-117">PARAMETERS</span></span>

### <span data-ttu-id="cd6cf-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="cd6cf-118">-AgreementContent</span></span>
<span data-ttu-id="cd6cf-119">Определяет содержимое соглашения в формате JavaScript Object Notation (JSON) для соглашения.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="cd6cf-120">Укажите либо этот параметр, либо параметр *AgreementContentFilePath* .</span><span class="sxs-lookup"><span data-stu-id="cd6cf-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="cd6cf-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="cd6cf-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="cd6cf-122">Задает путь к файлу соглашения для соглашения.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="cd6cf-123">Укажите либо этот параметр, либо параметр *AgreementContent* .</span><span class="sxs-lookup"><span data-stu-id="cd6cf-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="cd6cf-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="cd6cf-124">-AgreementName</span></span>
<span data-ttu-id="cd6cf-125">Указывает имя для соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="cd6cf-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="cd6cf-126">-AgreementType</span></span>
<span data-ttu-id="cd6cf-127">Указывает тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="cd6cf-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cd6cf-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd6cf-129">X12</span><span class="sxs-lookup"><span data-stu-id="cd6cf-129">X12</span></span> 
- <span data-ttu-id="cd6cf-130">AS2</span><span class="sxs-lookup"><span data-stu-id="cd6cf-130">AS2</span></span>
- <span data-ttu-id="cd6cf-131">Edifact</span><span class="sxs-lookup"><span data-stu-id="cd6cf-131">Edifact</span></span>

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

### <span data-ttu-id="cd6cf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6cf-132">-DefaultProfile</span></span>
<span data-ttu-id="cd6cf-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cd6cf-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd6cf-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="cd6cf-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="cd6cf-135">Указывает идентификационный ограничитель имени для гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="cd6cf-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="cd6cf-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="cd6cf-137">Значение описателя идентификации гостя для соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="cd6cf-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="cd6cf-138">-GuestPartner</span></span>
<span data-ttu-id="cd6cf-139">Указывает имя гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="cd6cf-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="cd6cf-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="cd6cf-141">Указывает классификатор имени бизнес-удостоверения для партнера узла.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="cd6cf-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="cd6cf-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="cd6cf-143">Значение описателя идентификатора узла для соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="cd6cf-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="cd6cf-144">-HostPartner</span></span>
<span data-ttu-id="cd6cf-145">Указывает имя партнера узла.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="cd6cf-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cd6cf-146">-Metadata</span></span>
<span data-ttu-id="cd6cf-147">Указывает объект метаданных для соглашения.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-147">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="cd6cf-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd6cf-148">-Name</span></span>
<span data-ttu-id="cd6cf-149">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-149">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="cd6cf-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6cf-150">-ResourceGroupName</span></span>
<span data-ttu-id="cd6cf-151">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cd6cf-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd6cf-152">-Confirm</span></span>
<span data-ttu-id="cd6cf-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd6cf-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd6cf-154">-WhatIf</span></span>
<span data-ttu-id="cd6cf-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd6cf-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd6cf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6cf-157">CommonParameters</span></span>
<span data-ttu-id="cd6cf-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6cf-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6cf-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6cf-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd6cf-160">INPUTS</span></span>

### <span data-ttu-id="cd6cf-161">System. String</span><span class="sxs-lookup"><span data-stu-id="cd6cf-161">System.String</span></span>

## <span data-ttu-id="cd6cf-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd6cf-162">OUTPUTS</span></span>

### <span data-ttu-id="cd6cf-163">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cd6cf-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="cd6cf-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd6cf-164">NOTES</span></span>

## <span data-ttu-id="cd6cf-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd6cf-165">RELATED LINKS</span></span>

[<span data-ttu-id="cd6cf-166">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cd6cf-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cd6cf-167">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cd6cf-167">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cd6cf-168">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cd6cf-168">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


