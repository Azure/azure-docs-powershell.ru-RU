---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 63241b764576e06166e293f17717b26c4dcbe3d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567120"
---
# <span data-ttu-id="f49aa-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f49aa-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="f49aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f49aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f49aa-103">Удаление соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f49aa-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f49aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f49aa-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f49aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f49aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f49aa-106">Командлет **Remove-AzureRmIntegrationAccountAgreement** удаляет соглашение с учетной записью интеграции из группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f49aa-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="f49aa-107">Укажите имя учетной записи интеграции, имя группы ресурсов и название соглашения.</span><span class="sxs-lookup"><span data-stu-id="f49aa-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="f49aa-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="f49aa-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f49aa-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="f49aa-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f49aa-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f49aa-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f49aa-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f49aa-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f49aa-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f49aa-112">EXAMPLES</span></span>

### <span data-ttu-id="f49aa-113">Пример 1: Удаление соглашения с учетной записью интеграции по имени</span><span class="sxs-lookup"><span data-stu-id="f49aa-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="f49aa-114">Эта команда удаляет соглашение с учетной записью интеграции с именем IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="f49aa-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="f49aa-115">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f49aa-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f49aa-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f49aa-116">PARAMETERS</span></span>

### <span data-ttu-id="f49aa-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="f49aa-117">-AgreementName</span></span>
<span data-ttu-id="f49aa-118">Указывает имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f49aa-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="f49aa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f49aa-119">-Force</span></span>
<span data-ttu-id="f49aa-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f49aa-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f49aa-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f49aa-121">-Name</span></span>
<span data-ttu-id="f49aa-122">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f49aa-122">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f49aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="f49aa-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f49aa-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f49aa-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f49aa-125">-Confirm</span></span>
<span data-ttu-id="f49aa-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f49aa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f49aa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f49aa-127">-WhatIf</span></span>
<span data-ttu-id="f49aa-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f49aa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f49aa-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f49aa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f49aa-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49aa-130">-DefaultProfile</span></span>
<span data-ttu-id="f49aa-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f49aa-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f49aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49aa-132">CommonParameters</span></span>
<span data-ttu-id="f49aa-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f49aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49aa-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f49aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49aa-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f49aa-135">INPUTS</span></span>

## <span data-ttu-id="f49aa-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f49aa-136">OUTPUTS</span></span>

## <span data-ttu-id="f49aa-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f49aa-137">NOTES</span></span>

## <span data-ttu-id="f49aa-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f49aa-138">RELATED LINKS</span></span>

[<span data-ttu-id="f49aa-139">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f49aa-139">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="f49aa-140">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f49aa-140">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="f49aa-141">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f49aa-141">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


