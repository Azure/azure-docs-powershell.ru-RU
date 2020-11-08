---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245735"
---
# <span data-ttu-id="52723-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="52723-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="52723-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52723-102">SYNOPSIS</span></span>
<span data-ttu-id="52723-103">Получает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="52723-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="52723-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52723-104">SYNTAX</span></span>

### <span data-ttu-id="52723-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="52723-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52723-106">S2</span><span class="sxs-lookup"><span data-stu-id="52723-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52723-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52723-107">DESCRIPTION</span></span>
<span data-ttu-id="52723-108">Командлет **Get-AzWebAppSlot** получает сведения о слоте веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="52723-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="52723-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52723-109">EXAMPLES</span></span>

### <span data-ttu-id="52723-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52723-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="52723-111">Эта команда получает слот с именем Slot001 из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="52723-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="52723-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52723-112">PARAMETERS</span></span>

### <span data-ttu-id="52723-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52723-113">-DefaultProfile</span></span>
<span data-ttu-id="52723-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52723-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52723-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52723-115">-Name</span></span>
<span data-ttu-id="52723-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="52723-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52723-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52723-117">-ResourceGroupName</span></span>
<span data-ttu-id="52723-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="52723-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52723-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="52723-119">-Slot</span></span>
<span data-ttu-id="52723-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="52723-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52723-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="52723-121">-WebApp</span></span>
<span data-ttu-id="52723-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="52723-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52723-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52723-123">CommonParameters</span></span>
<span data-ttu-id="52723-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52723-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52723-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52723-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52723-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52723-126">INPUTS</span></span>

### <span data-ttu-id="52723-127">System. String</span><span class="sxs-lookup"><span data-stu-id="52723-127">System.String</span></span>

### <span data-ttu-id="52723-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="52723-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="52723-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52723-129">OUTPUTS</span></span>

### <span data-ttu-id="52723-130">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="52723-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="52723-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="52723-131">NOTES</span></span>

## <span data-ttu-id="52723-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52723-132">RELATED LINKS</span></span>

[<span data-ttu-id="52723-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="52723-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="52723-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="52723-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="52723-135">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="52723-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="52723-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="52723-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="52723-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="52723-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="52723-138">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="52723-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="52723-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="52723-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
