---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912227"
---
# <span data-ttu-id="b1cb1-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="b1cb1-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="b1cb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cb1-103">Этот командлет извлекает текущее значение сгенерированного номера элемента управления обменом для каждого соглашения.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="b1cb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1cb1-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1cb1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="b1cb1-106">Этот командлет предназначен для использования в сценариях аварийного восстановления, чтобы получить текущее значение сгенерированного номера элемента управления обменом, чтобы повторно записать увеличенное значение с помощью Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="b1cb1-107">Номер элемента управления различностью следует увеличить, чтобы избежать дублирования номеров управления обменом для номеров, которые еще не были реплицированы в пассивную область при аварии в активном регионе.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="b1cb1-108">Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT</span><span class="sxs-lookup"><span data-stu-id="b1cb1-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="b1cb1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1cb1-109">EXAMPLES</span></span>

### <span data-ttu-id="b1cb1-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1cb1-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="b1cb1-111">Эта команда используется для того, чтобы создать учетную запись для интеграции, созданную X12 управления ключами для наименования соглашения.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="b1cb1-112">Убедитесь, что указанный контракт имеет тип "X12".</span><span class="sxs-lookup"><span data-stu-id="b1cb1-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="b1cb1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b1cb1-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="b1cb1-114">Эта команда используется для того, чтобы создать учетную запись для интеграции, созданную EDIFACT управления ключами для наименования соглашения.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="b1cb1-115">Убедитесь, что указанный контракт имеет тип "EDIFACT".</span><span class="sxs-lookup"><span data-stu-id="b1cb1-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="b1cb1-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b1cb1-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="b1cb1-117">Эта команда получает все созданные X12 элементы управления для обмена данными с именем учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="b1cb1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1cb1-118">PARAMETERS</span></span>

### <span data-ttu-id="b1cb1-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="b1cb1-119">-AgreementName</span></span>
<span data-ttu-id="b1cb1-120">Имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="b1cb1-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="b1cb1-121">-AgreementType</span></span>
<span data-ttu-id="b1cb1-122">Тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-122">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cb1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1cb1-123">-DefaultProfile</span></span>
<span data-ttu-id="b1cb1-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b1cb1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1cb1-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1cb1-125">-Name</span></span>
<span data-ttu-id="b1cb1-126">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-126">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cb1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1cb1-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1cb1-128">Имя группы ресурсов для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="b1cb1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cb1-129">CommonParameters</span></span>
<span data-ttu-id="b1cb1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cb1-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1cb1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cb1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1cb1-132">INPUTS</span></span>

### <span data-ttu-id="b1cb1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b1cb1-133">System.String</span></span>

## <span data-ttu-id="b1cb1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1cb1-134">OUTPUTS</span></span>

### <span data-ttu-id="b1cb1-135">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="b1cb1-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="b1cb1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1cb1-136">NOTES</span></span>

## <span data-ttu-id="b1cb1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1cb1-137">RELATED LINKS</span></span>

[<span data-ttu-id="b1cb1-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="b1cb1-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

