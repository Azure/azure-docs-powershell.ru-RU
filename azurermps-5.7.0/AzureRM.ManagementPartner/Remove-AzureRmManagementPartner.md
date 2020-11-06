---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 703c38d02ef6a6a339c58c861961cd2ad92ecb7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566618"
---
# <span data-ttu-id="734f7-101">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="734f7-101">Remove-AzureRmManagementPartner</span></span>

## <span data-ttu-id="734f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="734f7-102">SYNOPSIS</span></span>
<span data-ttu-id="734f7-103">Удалите идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="734f7-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="734f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="734f7-104">SYNTAX</span></span>

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="734f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="734f7-105">DESCRIPTION</span></span>
<span data-ttu-id="734f7-106">Удалите идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="734f7-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="734f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="734f7-107">EXAMPLES</span></span>

### <span data-ttu-id="734f7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="734f7-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="734f7-109">Удаление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="734f7-109">Remove management partner</span></span> 

## <span data-ttu-id="734f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="734f7-110">PARAMETERS</span></span>

### <span data-ttu-id="734f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734f7-111">-DefaultProfile</span></span>
<span data-ttu-id="734f7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="734f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="734f7-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="734f7-113">-PartnerId</span></span>
<span data-ttu-id="734f7-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="734f7-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734f7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="734f7-115">-PassThru</span></span>
<span data-ttu-id="734f7-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="734f7-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="734f7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="734f7-117">-Confirm</span></span>
<span data-ttu-id="734f7-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="734f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="734f7-119">-WhatIf</span></span>
<span data-ttu-id="734f7-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="734f7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="734f7-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="734f7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734f7-122">CommonParameters</span></span>
<span data-ttu-id="734f7-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="734f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734f7-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="734f7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734f7-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="734f7-125">INPUTS</span></span>

### <span data-ttu-id="734f7-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="734f7-126">None</span></span>

## <span data-ttu-id="734f7-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="734f7-127">OUTPUTS</span></span>

### <span data-ttu-id="734f7-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="734f7-128">System.Object</span></span>

## <span data-ttu-id="734f7-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="734f7-129">NOTES</span></span>

## <span data-ttu-id="734f7-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="734f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="734f7-131">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="734f7-131">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="734f7-132">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="734f7-132">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="734f7-133">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="734f7-133">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
