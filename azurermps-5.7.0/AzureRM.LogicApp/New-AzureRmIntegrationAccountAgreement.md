---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 838191018c50856f92f82699f7ac54686f1b3d97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733048"
---
# <span data-ttu-id="f6a68-101">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f6a68-101">New-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="f6a68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6a68-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a68-103">Создание соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a68-103">Creates an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6a68-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6a68-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a68-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a68-106">Командлет **New-AzureRmIntegrationAccountAgreement** создает соглашение с учетной записью интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a68-106">The **New-AzureRmIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="f6a68-107">Этот командлет возвращает объект, представляющий соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a68-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="f6a68-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя соглашения, тип, имя партнера, классификаторы партнеров и содержимое соглашения.</span><span class="sxs-lookup"><span data-stu-id="f6a68-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>

<span data-ttu-id="f6a68-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="f6a68-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="f6a68-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="f6a68-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f6a68-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="f6a68-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f6a68-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f6a68-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f6a68-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f6a68-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f6a68-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6a68-114">EXAMPLES</span></span>

### <span data-ttu-id="f6a68-115">Пример 1: создание соглашения для учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="f6a68-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="f6a68-116">Эта команда создает соглашение с учетной записью интеграции в указанной группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a68-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="f6a68-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6a68-117">PARAMETERS</span></span>

### <span data-ttu-id="f6a68-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="f6a68-118">-AgreementContent</span></span>
<span data-ttu-id="f6a68-119">Определяет содержимое соглашения в формате JavaScript Object Notation (JSON) для соглашения.</span><span class="sxs-lookup"><span data-stu-id="f6a68-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="f6a68-120">Укажите либо этот параметр, либо параметр *AgreementContentFilePath* .</span><span class="sxs-lookup"><span data-stu-id="f6a68-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="f6a68-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="f6a68-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="f6a68-122">Задает путь к файлу соглашения для соглашения.</span><span class="sxs-lookup"><span data-stu-id="f6a68-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="f6a68-123">Укажите либо этот параметр, либо параметр *AgreementContent* .</span><span class="sxs-lookup"><span data-stu-id="f6a68-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="f6a68-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="f6a68-124">-AgreementName</span></span>
<span data-ttu-id="f6a68-125">Указывает имя для соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a68-125">Specifies a name for the integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="f6a68-126">-AgreementType</span></span>
<span data-ttu-id="f6a68-127">Указывает тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a68-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="f6a68-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f6a68-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6a68-129">X12</span><span class="sxs-lookup"><span data-stu-id="f6a68-129">X12</span></span> 
- <span data-ttu-id="f6a68-130">AS2</span><span class="sxs-lookup"><span data-stu-id="f6a68-130">AS2</span></span>
- <span data-ttu-id="f6a68-131">Edifact</span><span class="sxs-lookup"><span data-stu-id="f6a68-131">Edifact</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a68-132">-DefaultProfile</span></span>
<span data-ttu-id="f6a68-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6a68-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6a68-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="f6a68-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="f6a68-135">Указывает идентификационный ограничитель имени для гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="f6a68-135">Specifies a name business identity qualifier for the guest partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="f6a68-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="f6a68-137">Значение описателя идентификации гостя для соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a68-137">The integration account agreement guest identity qualifier value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="f6a68-138">-GuestPartner</span></span>
<span data-ttu-id="f6a68-139">Указывает имя гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="f6a68-139">Specifies the name of the guest partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="f6a68-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="f6a68-141">Указывает классификатор имени бизнес-удостоверения для партнера узла.</span><span class="sxs-lookup"><span data-stu-id="f6a68-141">Specifies a name business identity qualifier for the host partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="f6a68-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="f6a68-143">Значение описателя идентификатора узла для соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a68-143">The integration account agreement host identity qualifier value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="f6a68-144">-HostPartner</span></span>
<span data-ttu-id="f6a68-145">Указывает имя партнера узла.</span><span class="sxs-lookup"><span data-stu-id="f6a68-145">Specifies the name of the host partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f6a68-146">-Metadata</span></span>
<span data-ttu-id="f6a68-147">Указывает объект метаданных для соглашения.</span><span class="sxs-lookup"><span data-stu-id="f6a68-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6a68-148">-Name</span></span>
<span data-ttu-id="f6a68-149">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6a68-149">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a68-150">-ResourceGroupName</span></span>
<span data-ttu-id="f6a68-151">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6a68-151">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6a68-152">-Confirm</span></span>
<span data-ttu-id="f6a68-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6a68-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a68-154">-WhatIf</span></span>
<span data-ttu-id="f6a68-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6a68-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6a68-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6a68-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a68-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a68-157">CommonParameters</span></span>
<span data-ttu-id="f6a68-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6a68-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a68-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a68-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a68-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6a68-160">INPUTS</span></span>

### <span data-ttu-id="f6a68-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="f6a68-161">None</span></span>
<span data-ttu-id="f6a68-162">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f6a68-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6a68-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a68-163">OUTPUTS</span></span>

### <span data-ttu-id="f6a68-164">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f6a68-164">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="f6a68-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6a68-165">NOTES</span></span>

## <span data-ttu-id="f6a68-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6a68-166">RELATED LINKS</span></span>

[<span data-ttu-id="f6a68-167">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f6a68-167">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="f6a68-168">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f6a68-168">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="f6a68-169">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f6a68-169">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


