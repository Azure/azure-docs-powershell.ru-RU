---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4d8091c4335bbba9574c112675bd4bdbbcaea662
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728348"
---
# <span data-ttu-id="849ab-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="849ab-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="849ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="849ab-102">SYNOPSIS</span></span>
<span data-ttu-id="849ab-103">Получает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="849ab-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="849ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="849ab-104">SYNTAX</span></span>

### <span data-ttu-id="849ab-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="849ab-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="849ab-106">S2</span><span class="sxs-lookup"><span data-stu-id="849ab-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="849ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="849ab-107">DESCRIPTION</span></span>
<span data-ttu-id="849ab-108">Командлет **Get-AzWebAppSlot** получает сведения о слоте веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="849ab-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="849ab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="849ab-109">EXAMPLES</span></span>

### <span data-ttu-id="849ab-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="849ab-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="849ab-111">Эта команда получает слот с именем Slot001 из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="849ab-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="849ab-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="849ab-112">PARAMETERS</span></span>

### <span data-ttu-id="849ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849ab-113">-DefaultProfile</span></span>
<span data-ttu-id="849ab-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="849ab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="849ab-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="849ab-115">-Name</span></span>
<span data-ttu-id="849ab-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="849ab-116">WebApp Name</span></span>

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

### <span data-ttu-id="849ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="849ab-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="849ab-118">Resource Group Name</span></span>

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

### <span data-ttu-id="849ab-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="849ab-119">-Slot</span></span>
<span data-ttu-id="849ab-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="849ab-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="849ab-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="849ab-121">-WebApp</span></span>
<span data-ttu-id="849ab-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="849ab-122">WebApp Object</span></span>

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

### <span data-ttu-id="849ab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849ab-123">CommonParameters</span></span>
<span data-ttu-id="849ab-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="849ab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849ab-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="849ab-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849ab-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="849ab-126">INPUTS</span></span>

### <span data-ttu-id="849ab-127">System. String</span><span class="sxs-lookup"><span data-stu-id="849ab-127">System.String</span></span>

### <span data-ttu-id="849ab-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="849ab-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="849ab-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="849ab-129">OUTPUTS</span></span>

### <span data-ttu-id="849ab-130">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="849ab-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="849ab-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="849ab-131">NOTES</span></span>

## <span data-ttu-id="849ab-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="849ab-132">RELATED LINKS</span></span>

[<span data-ttu-id="849ab-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="849ab-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="849ab-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="849ab-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="849ab-135">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="849ab-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="849ab-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="849ab-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="849ab-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="849ab-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="849ab-138">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="849ab-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="849ab-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="849ab-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
