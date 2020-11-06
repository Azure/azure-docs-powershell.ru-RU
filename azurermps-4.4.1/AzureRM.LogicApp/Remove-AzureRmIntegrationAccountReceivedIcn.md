---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 95c2b33b52ed9660c57aad35128af4eba277c0a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567599"
---
# <span data-ttu-id="02c05-101">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="02c05-101">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="02c05-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02c05-102">SYNOPSIS</span></span>
<span data-ttu-id="02c05-103">Этот командлет удаляет определенный полученный номер, указанный в параметрах управления обменом, для каждого соглашения и номера элемента управления.</span><span class="sxs-lookup"><span data-stu-id="02c05-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02c05-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02c05-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c05-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02c05-105">DESCRIPTION</span></span>
<span data-ttu-id="02c05-106">Этот командлет используется в сценариях аварийного восстановления для удаления полученного номера управления обменом из учетной записи интеграции, чтобы соединитель B2B мог обработать сообщение повторно, если включено обнаружение дубликатов номеров.</span><span class="sxs-lookup"><span data-stu-id="02c05-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="02c05-107">В редких случаях полученный номер управления обменом может быть зарезервирован вскоре до аварии и до тех пор, пока соединитель B2B не отклоняет обмен как ошибочный.</span><span class="sxs-lookup"><span data-stu-id="02c05-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="02c05-108">В таких случаях может потребоваться, чтобы веб-сайт восстановления повторно мог обработать тот же обмен после его устранения.</span><span class="sxs-lookup"><span data-stu-id="02c05-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="02c05-109">Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT</span><span class="sxs-lookup"><span data-stu-id="02c05-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="02c05-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02c05-110">EXAMPLES</span></span>

### <span data-ttu-id="02c05-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02c05-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="02c05-112">Пытается получить полученный X12ный управляющий номер, который не является допустимым форматом содержимого.</span><span class="sxs-lookup"><span data-stu-id="02c05-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="02c05-113">Удаляет полученный X12ный номер управления обменом.</span><span class="sxs-lookup"><span data-stu-id="02c05-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="02c05-114">Подтверждение того, что полученный номер элемента управления X12 Interchange был удален, пытаясь получить его еще раз.</span><span class="sxs-lookup"><span data-stu-id="02c05-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="02c05-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="02c05-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="02c05-116">Пытается получить полученный Edifactный управляющий номер, который не является допустимым форматом содержимого.</span><span class="sxs-lookup"><span data-stu-id="02c05-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="02c05-117">Удаляет полученный Edifactный номер управления обменом.</span><span class="sxs-lookup"><span data-stu-id="02c05-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="02c05-118">Подтверждение того, что полученный номер элемента управления EDIFACT Interchange был удален, пытаясь получить его еще раз.</span><span class="sxs-lookup"><span data-stu-id="02c05-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="02c05-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02c05-119">PARAMETERS</span></span>

### <span data-ttu-id="02c05-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="02c05-120">-AgreementName</span></span>
<span data-ttu-id="02c05-121">Имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="02c05-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="02c05-122">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="02c05-122">-ControlNumberValue</span></span>
<span data-ttu-id="02c05-123">Значение номера контроля учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="02c05-123">The integration account control number value.</span></span>

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

### <span data-ttu-id="02c05-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02c05-124">-Name</span></span>
<span data-ttu-id="02c05-125">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="02c05-125">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c05-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c05-126">-ResourceGroupName</span></span>
<span data-ttu-id="02c05-127">Имя группы ресурсов для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="02c05-127">The integration account resource group name.</span></span>

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

### <span data-ttu-id="02c05-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02c05-128">-Confirm</span></span>
<span data-ttu-id="02c05-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02c05-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c05-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c05-130">-WhatIf</span></span>
<span data-ttu-id="02c05-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02c05-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c05-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02c05-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c05-133">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="02c05-133">-AgreementType</span></span>
<span data-ttu-id="02c05-134">Тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="02c05-134">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c05-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c05-135">-DefaultProfile</span></span>
<span data-ttu-id="02c05-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02c05-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02c05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c05-137">CommonParameters</span></span>
<span data-ttu-id="02c05-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02c05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c05-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c05-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c05-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02c05-140">INPUTS</span></span>

### <span data-ttu-id="02c05-141">System. String</span><span class="sxs-lookup"><span data-stu-id="02c05-141">System.String</span></span>

## <span data-ttu-id="02c05-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02c05-142">OUTPUTS</span></span>

### <span data-ttu-id="02c05-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="02c05-143">System.Object</span></span>

## <span data-ttu-id="02c05-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="02c05-144">NOTES</span></span>

## <span data-ttu-id="02c05-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02c05-145">RELATED LINKS</span></span>

<span data-ttu-id="02c05-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="02c05-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span></span>

