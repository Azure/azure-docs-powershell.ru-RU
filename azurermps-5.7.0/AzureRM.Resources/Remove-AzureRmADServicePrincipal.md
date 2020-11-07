---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733222"
---
# <span data-ttu-id="f9ad4-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f9ad4-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="f9ad4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ad4-103">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9ad4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9ad4-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ad4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9ad4-105">DESCRIPTION</span></span>
<span data-ttu-id="f9ad4-106">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="f9ad4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9ad4-107">EXAMPLES</span></span>

### <span data-ttu-id="f9ad4-108">Удаление субъекта-службы AAD.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="f9ad4-109">Удаляет заданного субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="f9ad4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9ad4-110">PARAMETERS</span></span>

### <span data-ttu-id="f9ad4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ad4-111">-DefaultProfile</span></span>
<span data-ttu-id="f9ad4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f9ad4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9ad4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f9ad4-113">-Force</span></span>
<span data-ttu-id="f9ad4-114">{Определение принудительной заливки}}</span><span class="sxs-lookup"><span data-stu-id="f9ad4-114">{{Fill Force Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad4-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f9ad4-115">-ObjectId</span></span>
<span data-ttu-id="f9ad4-116">Идентификатор объекта субъекта-службы, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9ad4-117">-PassThru</span></span>
<span data-ttu-id="f9ad4-118">Если указан, возвращает участника-службы.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-118">If specified, returns the deleted service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9ad4-119">-Confirm</span></span>
<span data-ttu-id="f9ad4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ad4-121">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ad4-122">CommonParameters</span></span>
<span data-ttu-id="f9ad4-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ad4-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9ad4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ad4-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9ad4-125">INPUTS</span></span>

### <span data-ttu-id="f9ad4-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="f9ad4-126">None</span></span>
<span data-ttu-id="f9ad4-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9ad4-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9ad4-128">OUTPUTS</span></span>

### <span data-ttu-id="f9ad4-129">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f9ad4-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f9ad4-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9ad4-130">NOTES</span></span>
<span data-ttu-id="f9ad4-131">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="f9ad4-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f9ad4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9ad4-132">RELATED LINKS</span></span>

[<span data-ttu-id="f9ad4-133">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f9ad4-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f9ad4-134">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f9ad4-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f9ad4-135">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f9ad4-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f9ad4-136">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f9ad4-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="f9ad4-137">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f9ad4-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
