---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733626"
---
# <span data-ttu-id="32239-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32239-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="32239-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32239-102">SYNOPSIS</span></span>
<span data-ttu-id="32239-103">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32239-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32239-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32239-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32239-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32239-105">DESCRIPTION</span></span>
<span data-ttu-id="32239-106">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32239-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="32239-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32239-107">EXAMPLES</span></span>

### <span data-ttu-id="32239-108">--------------------------Удалить субъекта-службы AAD.</span><span class="sxs-lookup"><span data-stu-id="32239-108">--------------------------  Delete AAD service principal.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="32239-109">Удаляет заданного субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32239-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="32239-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32239-110">PARAMETERS</span></span>

### <span data-ttu-id="32239-111">-Force</span><span class="sxs-lookup"><span data-stu-id="32239-111">-Force</span></span>
<span data-ttu-id="32239-112">{Определение принудительной заливки}}</span><span class="sxs-lookup"><span data-stu-id="32239-112">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="32239-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="32239-113">-ObjectId</span></span>
<span data-ttu-id="32239-114">Идентификатор объекта субъекта-службы, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="32239-114">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32239-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32239-115">-PassThru</span></span>
<span data-ttu-id="32239-116">Если указан, возвращает участника-службы.</span><span class="sxs-lookup"><span data-stu-id="32239-116">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="32239-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32239-117">-Confirm</span></span>
<span data-ttu-id="32239-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32239-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32239-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32239-119">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32239-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32239-120">-DefaultProfile</span></span>
<span data-ttu-id="32239-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32239-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32239-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32239-122">CommonParameters</span></span>
<span data-ttu-id="32239-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32239-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32239-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32239-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32239-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32239-125">INPUTS</span></span>

## <span data-ttu-id="32239-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32239-126">OUTPUTS</span></span>

### <span data-ttu-id="32239-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32239-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="32239-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="32239-128">NOTES</span></span>
<span data-ttu-id="32239-129">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="32239-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="32239-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32239-130">RELATED LINKS</span></span>

[<span data-ttu-id="32239-131">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32239-131">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="32239-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32239-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="32239-133">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32239-133">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="32239-134">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="32239-134">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="32239-135">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="32239-135">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
