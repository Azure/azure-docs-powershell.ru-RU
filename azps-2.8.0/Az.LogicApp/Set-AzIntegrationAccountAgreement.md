---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: fa03a9a14c8024298656de1ed8bcf97bbf65378c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720487"
---
# <span data-ttu-id="8bf27-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8bf27-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="8bf27-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bf27-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf27-103">Изменение соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="8bf27-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="8bf27-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bf27-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bf27-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bf27-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf27-106">Командлет **Set-AzIntegrationAccountAgreement** изменяет соглашение с учетной записью интеграции.</span><span class="sxs-lookup"><span data-stu-id="8bf27-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="8bf27-107">Этот командлет возвращает объект, представляющий соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="8bf27-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="8bf27-108">Укажите имя учетной записи интеграции, имя группы ресурсов и название соглашения.</span><span class="sxs-lookup"><span data-stu-id="8bf27-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="8bf27-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="8bf27-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="8bf27-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="8bf27-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8bf27-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="8bf27-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8bf27-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="8bf27-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8bf27-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="8bf27-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8bf27-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bf27-114">EXAMPLES</span></span>

### <span data-ttu-id="8bf27-115">Пример 1: обновление соглашения с учетной записью интеграции</span><span class="sxs-lookup"><span data-stu-id="8bf27-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="8bf27-116">Эта команда обновляет соглашение с учетной записью интеграции в указанной группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf27-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="8bf27-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bf27-117">PARAMETERS</span></span>

### <span data-ttu-id="8bf27-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="8bf27-118">-AgreementContent</span></span>
<span data-ttu-id="8bf27-119">Определяет содержимое соглашения в формате JavaScript Object Notation (JSON) для соглашения.</span><span class="sxs-lookup"><span data-stu-id="8bf27-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="8bf27-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="8bf27-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="8bf27-121">Задает путь к файлу соглашения для соглашения.</span><span class="sxs-lookup"><span data-stu-id="8bf27-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="8bf27-122">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="8bf27-122">-AgreementName</span></span>
<span data-ttu-id="8bf27-123">Указывает имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="8bf27-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="8bf27-124">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="8bf27-124">-AgreementType</span></span>
<span data-ttu-id="8bf27-125">Указывает тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="8bf27-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="8bf27-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8bf27-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8bf27-127">X12</span><span class="sxs-lookup"><span data-stu-id="8bf27-127">X12</span></span> 
- <span data-ttu-id="8bf27-128">AS2</span><span class="sxs-lookup"><span data-stu-id="8bf27-128">AS2</span></span>
- <span data-ttu-id="8bf27-129">Edifact</span><span class="sxs-lookup"><span data-stu-id="8bf27-129">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf27-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf27-130">-DefaultProfile</span></span>
<span data-ttu-id="8bf27-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8bf27-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bf27-132">-Force</span><span class="sxs-lookup"><span data-stu-id="8bf27-132">-Force</span></span>
<span data-ttu-id="8bf27-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8bf27-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf27-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="8bf27-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="8bf27-135">Указывает идентификационный ограничитель имени для гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="8bf27-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="8bf27-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="8bf27-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="8bf27-137">Значение описателя идентификации гостя для соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="8bf27-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="8bf27-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="8bf27-138">-GuestPartner</span></span>
<span data-ttu-id="8bf27-139">Указывает имя гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="8bf27-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="8bf27-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="8bf27-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="8bf27-141">Указывает классификатор имени бизнес-удостоверения для партнера узла.</span><span class="sxs-lookup"><span data-stu-id="8bf27-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="8bf27-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="8bf27-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="8bf27-143">Значение описателя идентификатора узла для соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="8bf27-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="8bf27-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="8bf27-144">-HostPartner</span></span>
<span data-ttu-id="8bf27-145">Указывает имя партнера узла.</span><span class="sxs-lookup"><span data-stu-id="8bf27-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="8bf27-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8bf27-146">-Metadata</span></span>
<span data-ttu-id="8bf27-147">Указывает объект метаданных для соглашения.</span><span class="sxs-lookup"><span data-stu-id="8bf27-147">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="8bf27-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8bf27-148">-Name</span></span>
<span data-ttu-id="8bf27-149">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="8bf27-149">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="8bf27-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf27-150">-ResourceGroupName</span></span>
<span data-ttu-id="8bf27-151">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8bf27-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8bf27-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bf27-152">-Confirm</span></span>
<span data-ttu-id="8bf27-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8bf27-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bf27-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf27-154">-WhatIf</span></span>
<span data-ttu-id="8bf27-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8bf27-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf27-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8bf27-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bf27-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf27-157">CommonParameters</span></span>
<span data-ttu-id="8bf27-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bf27-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf27-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf27-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf27-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bf27-160">INPUTS</span></span>

### <span data-ttu-id="8bf27-161">System. String</span><span class="sxs-lookup"><span data-stu-id="8bf27-161">System.String</span></span>

## <span data-ttu-id="8bf27-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bf27-162">OUTPUTS</span></span>

### <span data-ttu-id="8bf27-163">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8bf27-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="8bf27-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bf27-164">NOTES</span></span>

## <span data-ttu-id="8bf27-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bf27-165">RELATED LINKS</span></span>

[<span data-ttu-id="8bf27-166">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8bf27-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="8bf27-167">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8bf27-167">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="8bf27-168">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8bf27-168">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


