---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: eb78395274171f448076a4cd3ad9b6bac0093301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735164"
---
# <span data-ttu-id="962a1-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="962a1-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="962a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="962a1-102">SYNOPSIS</span></span>
<span data-ttu-id="962a1-103">Удаление учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="962a1-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="962a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="962a1-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="962a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="962a1-105">DESCRIPTION</span></span>
<span data-ttu-id="962a1-106">Командлет **Remove-AzureRmIntegrationAccount** удаляет учетную запись интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="962a1-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="962a1-107">Укажите имя учетной записи для интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="962a1-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="962a1-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="962a1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="962a1-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="962a1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="962a1-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="962a1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="962a1-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="962a1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="962a1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="962a1-112">EXAMPLES</span></span>

### <span data-ttu-id="962a1-113">Пример 1: Удаление учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="962a1-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="962a1-114">Эта команда удаляет учетную запись интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="962a1-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="962a1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="962a1-115">PARAMETERS</span></span>

### <span data-ttu-id="962a1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="962a1-116">-Force</span></span>
<span data-ttu-id="962a1-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="962a1-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="962a1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="962a1-118">-Name</span></span>
<span data-ttu-id="962a1-119">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="962a1-119">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="962a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="962a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="962a1-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="962a1-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="962a1-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="962a1-122">-Confirm</span></span>
<span data-ttu-id="962a1-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="962a1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="962a1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962a1-124">-WhatIf</span></span>
<span data-ttu-id="962a1-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="962a1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="962a1-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="962a1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="962a1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962a1-127">-DefaultProfile</span></span>
<span data-ttu-id="962a1-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="962a1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="962a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962a1-129">CommonParameters</span></span>
<span data-ttu-id="962a1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="962a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962a1-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962a1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962a1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="962a1-132">INPUTS</span></span>

## <span data-ttu-id="962a1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="962a1-133">OUTPUTS</span></span>

## <span data-ttu-id="962a1-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="962a1-134">NOTES</span></span>

## <span data-ttu-id="962a1-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="962a1-135">RELATED LINKS</span></span>

[<span data-ttu-id="962a1-136">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="962a1-136">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="962a1-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="962a1-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="962a1-138">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="962a1-138">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


