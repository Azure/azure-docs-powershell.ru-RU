---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074344"
---
# <span data-ttu-id="f1eac-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="f1eac-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="f1eac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1eac-102">SYNOPSIS</span></span>
<span data-ttu-id="f1eac-103">Возвращает URL-адрес обратного вызова триггера приложения логики.</span><span class="sxs-lookup"><span data-stu-id="f1eac-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="f1eac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1eac-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1eac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1eac-105">DESCRIPTION</span></span>
<span data-ttu-id="f1eac-106">Командлет **Get-AzLogicAppTriggerCallbackUrl** получает логическое приложение, вызывающее URL-адрес обратного вызова из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1eac-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="f1eac-107">Этот командлет возвращает объект **WorkflowTriggerCallbackUrl** , который представляет URL-адрес обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f1eac-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="f1eac-108">Укажите имя группы ресурсов, имя логического приложения и имя триггера.</span><span class="sxs-lookup"><span data-stu-id="f1eac-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="f1eac-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="f1eac-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f1eac-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="f1eac-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f1eac-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f1eac-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f1eac-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f1eac-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f1eac-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1eac-113">EXAMPLES</span></span>

### <span data-ttu-id="f1eac-114">Пример 1: получение URL-адреса обратного вызова триггера приложения логики</span><span class="sxs-lookup"><span data-stu-id="f1eac-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="f1eac-115">Эта команда возвращает URL-адрес обратного вызова триггера приложения логики.</span><span class="sxs-lookup"><span data-stu-id="f1eac-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="f1eac-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1eac-116">PARAMETERS</span></span>

### <span data-ttu-id="f1eac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1eac-117">-DefaultProfile</span></span>
<span data-ttu-id="f1eac-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f1eac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1eac-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1eac-119">-Name</span></span>
<span data-ttu-id="f1eac-120">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="f1eac-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1eac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1eac-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1eac-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1eac-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f1eac-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="f1eac-123">-TriggerName</span></span>
<span data-ttu-id="f1eac-124">Указывает имя триггера.</span><span class="sxs-lookup"><span data-stu-id="f1eac-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="f1eac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1eac-125">CommonParameters</span></span>
<span data-ttu-id="f1eac-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1eac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1eac-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1eac-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1eac-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1eac-128">INPUTS</span></span>

### <span data-ttu-id="f1eac-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f1eac-129">System.String</span></span>

## <span data-ttu-id="f1eac-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1eac-130">OUTPUTS</span></span>

### <span data-ttu-id="f1eac-131">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="f1eac-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="f1eac-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1eac-132">NOTES</span></span>

## <span data-ttu-id="f1eac-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1eac-133">RELATED LINKS</span></span>

[<span data-ttu-id="f1eac-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="f1eac-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


