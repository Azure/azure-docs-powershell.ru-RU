---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9374f8a55beca561afd9ed4bca4320b685349798
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2020
ms.locfileid: "94245138"
---
# <span data-ttu-id="684cb-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="684cb-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="684cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="684cb-102">SYNOPSIS</span></span>
<span data-ttu-id="684cb-103">Возвращает активацию моста Azure.</span><span class="sxs-lookup"><span data-stu-id="684cb-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="684cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="684cb-104">SYNTAX</span></span>

### <span data-ttu-id="684cb-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="684cb-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="684cb-106">Получить</span><span class="sxs-lookup"><span data-stu-id="684cb-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="684cb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="684cb-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="684cb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="684cb-108">DESCRIPTION</span></span>
<span data-ttu-id="684cb-109">После регистрации стека Azure объект активации содержит данные, которые связывают развертывание стека Azure с его регистрацией в Azure, например Дата окончания срока действия, имя и т. д.</span><span class="sxs-lookup"><span data-stu-id="684cb-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="684cb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="684cb-110">EXAMPLES</span></span>

### <span data-ttu-id="684cb-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="684cb-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="684cb-112">Получение списка активаций моста Azure в группе ресурсов "activationRG"</span><span class="sxs-lookup"><span data-stu-id="684cb-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="684cb-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="684cb-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="684cb-114">Получение активации моста Azure по имени "myActivation", расположенному в разделе "activationRG"</span><span class="sxs-lookup"><span data-stu-id="684cb-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="684cb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="684cb-115">PARAMETERS</span></span>

### <span data-ttu-id="684cb-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="684cb-116">-Name</span></span>
<span data-ttu-id="684cb-117">Имя активации.</span><span class="sxs-lookup"><span data-stu-id="684cb-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684cb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684cb-118">-ResourceGroupName</span></span>
<span data-ttu-id="684cb-119">Группа ресурсов, используемая во время регистрации стека Azure; Вы также можете просматривать имена групп ресурсов на портале.</span><span class="sxs-lookup"><span data-stu-id="684cb-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684cb-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="684cb-120">-ResourceId</span></span>
<span data-ttu-id="684cb-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="684cb-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="684cb-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="684cb-122">-Skip</span></span>
<span data-ttu-id="684cb-123">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="684cb-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684cb-124">-Top</span><span class="sxs-lookup"><span data-stu-id="684cb-124">-Top</span></span>
<span data-ttu-id="684cb-125">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="684cb-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="684cb-126">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="684cb-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684cb-127">CommonParameters</span></span>
<span data-ttu-id="684cb-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="684cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684cb-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="684cb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684cb-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="684cb-130">INPUTS</span></span>

## <span data-ttu-id="684cb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="684cb-131">OUTPUTS</span></span>

### <span data-ttu-id="684cb-132">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="684cb-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="684cb-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="684cb-133">NOTES</span></span>

## <span data-ttu-id="684cb-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="684cb-134">RELATED LINKS</span></span>