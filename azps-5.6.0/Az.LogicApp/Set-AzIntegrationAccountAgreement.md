---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 6c7781f5617571003083328adfac8aa7b349841b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962936"
---
# <span data-ttu-id="6a41b-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6a41b-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="6a41b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a41b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a41b-103">Изменяет соглашение об интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="6a41b-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="6a41b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a41b-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a41b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a41b-105">DESCRIPTION</span></span>
<span data-ttu-id="6a41b-106">**Cmdlet Set-AzIntegrationAccountAgreement** изменяет соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6a41b-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="6a41b-107">Этот cmdlet возвращает объект, который представляет соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6a41b-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="6a41b-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя соглашения.</span><span class="sxs-lookup"><span data-stu-id="6a41b-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="6a41b-109">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="6a41b-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="6a41b-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="6a41b-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6a41b-111">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="6a41b-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6a41b-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="6a41b-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6a41b-113">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="6a41b-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6a41b-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a41b-114">EXAMPLES</span></span>

### <span data-ttu-id="6a41b-115">Пример 1. Обновление соглашения об интеграции с учетной записью</span><span class="sxs-lookup"><span data-stu-id="6a41b-115">Example 1: Update an integration account agreement</span></span>
```powershell
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

<span data-ttu-id="6a41b-116">Эта команда обновляет соглашение об учетной записи интеграции в указанной группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6a41b-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="6a41b-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6a41b-117">Example 2</span></span>

<span data-ttu-id="6a41b-118">Изменяет соглашение об интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="6a41b-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="6a41b-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="6a41b-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="6a41b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a41b-120">PARAMETERS</span></span>

### <span data-ttu-id="6a41b-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="6a41b-121">-AgreementContent</span></span>
<span data-ttu-id="6a41b-122">Определяет содержимое соглашения в формате нотации объектов JavaScript (JSON) для соглашения.</span><span class="sxs-lookup"><span data-stu-id="6a41b-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="6a41b-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="6a41b-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="6a41b-124">Путь к файлу содержимого соглашения.</span><span class="sxs-lookup"><span data-stu-id="6a41b-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="6a41b-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="6a41b-125">-AgreementName</span></span>
<span data-ttu-id="6a41b-126">Указывает имя соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6a41b-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="6a41b-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="6a41b-127">-AgreementType</span></span>
<span data-ttu-id="6a41b-128">Указывает тип соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6a41b-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="6a41b-129">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="6a41b-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a41b-130">X12</span><span class="sxs-lookup"><span data-stu-id="6a41b-130">X12</span></span> 
- <span data-ttu-id="6a41b-131">AS2</span><span class="sxs-lookup"><span data-stu-id="6a41b-131">AS2</span></span>
- <span data-ttu-id="6a41b-132">Edifact</span><span class="sxs-lookup"><span data-stu-id="6a41b-132">Edifact</span></span>

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

### <span data-ttu-id="6a41b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a41b-133">-DefaultProfile</span></span>
<span data-ttu-id="6a41b-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6a41b-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a41b-135">-Force</span><span class="sxs-lookup"><span data-stu-id="6a41b-135">-Force</span></span>
<span data-ttu-id="6a41b-136">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6a41b-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a41b-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="6a41b-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="6a41b-138">Определяет для гостевого партнера квалификатор бизнес-удостоверений.</span><span class="sxs-lookup"><span data-stu-id="6a41b-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="6a41b-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="6a41b-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="6a41b-140">Значение гостевого удостоверения, установленное соглашением для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6a41b-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="6a41b-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="6a41b-141">-GuestPartner</span></span>
<span data-ttu-id="6a41b-142">Указывает имя гостевого партнера.</span><span class="sxs-lookup"><span data-stu-id="6a41b-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="6a41b-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="6a41b-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="6a41b-144">Определяет для партнера-хост-партнера квалификатор бизнес-удостоверений.</span><span class="sxs-lookup"><span data-stu-id="6a41b-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="6a41b-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="6a41b-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="6a41b-146">Значение квалификатора идентификаторов для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="6a41b-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="6a41b-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="6a41b-147">-HostPartner</span></span>
<span data-ttu-id="6a41b-148">Указывает имя партнера-ведущего.</span><span class="sxs-lookup"><span data-stu-id="6a41b-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="6a41b-149">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="6a41b-149">-Metadata</span></span>
<span data-ttu-id="6a41b-150">Указывает объект метаданных для соглашения.</span><span class="sxs-lookup"><span data-stu-id="6a41b-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="6a41b-151">-Name</span><span class="sxs-lookup"><span data-stu-id="6a41b-151">-Name</span></span>
<span data-ttu-id="6a41b-152">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6a41b-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="6a41b-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a41b-153">-ResourceGroupName</span></span>
<span data-ttu-id="6a41b-154">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a41b-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6a41b-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a41b-155">-Confirm</span></span>
<span data-ttu-id="6a41b-156">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6a41b-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a41b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a41b-157">-WhatIf</span></span>
<span data-ttu-id="6a41b-158">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a41b-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a41b-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6a41b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a41b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a41b-160">CommonParameters</span></span>
<span data-ttu-id="6a41b-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a41b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a41b-162">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a41b-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a41b-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a41b-163">INPUTS</span></span>

### <span data-ttu-id="6a41b-164">System.String</span><span class="sxs-lookup"><span data-stu-id="6a41b-164">System.String</span></span>

## <span data-ttu-id="6a41b-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a41b-165">OUTPUTS</span></span>

### <span data-ttu-id="6a41b-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountagreement</span><span class="sxs-lookup"><span data-stu-id="6a41b-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="6a41b-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a41b-167">NOTES</span></span>

## <span data-ttu-id="6a41b-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a41b-168">RELATED LINKS</span></span>

[<span data-ttu-id="6a41b-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6a41b-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="6a41b-170">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6a41b-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="6a41b-171">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6a41b-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


