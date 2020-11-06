---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567063"
---
# <span data-ttu-id="4fbfe-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4fbfe-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="4fbfe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fbfe-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbfe-103">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fbfe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fbfe-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fbfe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fbfe-105">DESCRIPTION</span></span>
<span data-ttu-id="4fbfe-106">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="4fbfe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fbfe-107">EXAMPLES</span></span>

### <span data-ttu-id="4fbfe-108">--------------------------Удалить приложение AAD.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="4fbfe-109">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="4fbfe-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fbfe-110">PARAMETERS</span></span>

### <span data-ttu-id="4fbfe-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4fbfe-111">-Force</span></span>
<span data-ttu-id="4fbfe-112">Переключение на удаление приложения без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-112">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="4fbfe-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4fbfe-113">-ObjectId</span></span>
<span data-ttu-id="4fbfe-114">Идентификатор объекта приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fbfe-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fbfe-115">-Confirm</span></span>
<span data-ttu-id="4fbfe-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fbfe-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fbfe-117">-WhatIf</span></span>
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

### <span data-ttu-id="4fbfe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbfe-118">-DefaultProfile</span></span>
<span data-ttu-id="4fbfe-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fbfe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbfe-120">CommonParameters</span></span>
<span data-ttu-id="4fbfe-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fbfe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbfe-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbfe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbfe-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fbfe-123">INPUTS</span></span>

## <span data-ttu-id="4fbfe-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fbfe-124">OUTPUTS</span></span>

## <span data-ttu-id="4fbfe-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fbfe-125">NOTES</span></span>
<span data-ttu-id="4fbfe-126">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="4fbfe-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4fbfe-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fbfe-127">RELATED LINKS</span></span>

[<span data-ttu-id="4fbfe-128">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4fbfe-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="4fbfe-129">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4fbfe-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="4fbfe-130">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4fbfe-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="4fbfe-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4fbfe-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

