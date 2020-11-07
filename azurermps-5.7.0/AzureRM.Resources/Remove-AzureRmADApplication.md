---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733225"
---
# <span data-ttu-id="c7626-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c7626-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="c7626-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7626-102">SYNOPSIS</span></span>
<span data-ttu-id="c7626-103">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c7626-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7626-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7626-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7626-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7626-105">DESCRIPTION</span></span>
<span data-ttu-id="c7626-106">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c7626-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="c7626-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7626-107">EXAMPLES</span></span>

### <span data-ttu-id="c7626-108">Удалите приложение AAD.</span><span class="sxs-lookup"><span data-stu-id="c7626-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="c7626-109">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c7626-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="c7626-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7626-110">PARAMETERS</span></span>

### <span data-ttu-id="c7626-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7626-111">-DefaultProfile</span></span>
<span data-ttu-id="c7626-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c7626-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7626-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c7626-113">-Force</span></span>
<span data-ttu-id="c7626-114">Переключение на удаление приложения без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c7626-114">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="c7626-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c7626-115">-ObjectId</span></span>
<span data-ttu-id="c7626-116">Идентификатор объекта приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c7626-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7626-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7626-117">-Confirm</span></span>
<span data-ttu-id="c7626-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7626-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7626-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7626-119">-WhatIf</span></span>
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

### <span data-ttu-id="c7626-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7626-120">CommonParameters</span></span>
<span data-ttu-id="c7626-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7626-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7626-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7626-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7626-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7626-123">INPUTS</span></span>

### <span data-ttu-id="c7626-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="c7626-124">None</span></span>
<span data-ttu-id="c7626-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c7626-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7626-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7626-126">OUTPUTS</span></span>

## <span data-ttu-id="c7626-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7626-127">NOTES</span></span>
<span data-ttu-id="c7626-128">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="c7626-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c7626-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7626-129">RELATED LINKS</span></span>

[<span data-ttu-id="c7626-130">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c7626-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="c7626-131">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c7626-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="c7626-132">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c7626-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="c7626-133">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7626-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

