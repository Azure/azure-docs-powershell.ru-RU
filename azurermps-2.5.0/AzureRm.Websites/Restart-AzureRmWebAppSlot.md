---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: ad3ff3dbd5589a890ecf7649c9a9b66843b8b444
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914969"
---
# <span data-ttu-id="39726-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39726-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="39726-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39726-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39726-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39726-103">SYNTAX</span></span>

### <span data-ttu-id="39726-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="39726-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39726-105">S2</span><span class="sxs-lookup"><span data-stu-id="39726-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39726-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39726-106">DESCRIPTION</span></span>
<span data-ttu-id="39726-107">Командлет **restarting-AzureRmWebAppSlot** останавливается, а затем запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="39726-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="39726-108">Если ячейка веб-приложения находится в остановленном состоянии, используйте командлет Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="39726-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="39726-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39726-109">EXAMPLES</span></span>

### <span data-ttu-id="39726-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39726-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="39726-111">Эта команда перезапускает слот Slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="39726-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="39726-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39726-112">PARAMETERS</span></span>

### <span data-ttu-id="39726-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39726-113">-DefaultProfile</span></span>
<span data-ttu-id="39726-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39726-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39726-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39726-115">-Name</span></span>
<span data-ttu-id="39726-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="39726-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39726-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39726-117">-ResourceGroupName</span></span>
<span data-ttu-id="39726-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="39726-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39726-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="39726-119">-Slot</span></span>
<span data-ttu-id="39726-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="39726-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39726-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="39726-121">-WebApp</span></span>
<span data-ttu-id="39726-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="39726-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39726-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39726-123">CommonParameters</span></span>
<span data-ttu-id="39726-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39726-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39726-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39726-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39726-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39726-126">INPUTS</span></span>

### <span data-ttu-id="39726-127">Семейств</span><span class="sxs-lookup"><span data-stu-id="39726-127">Site</span></span>
<span data-ttu-id="39726-128">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="39726-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="39726-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39726-129">OUTPUTS</span></span>

## <span data-ttu-id="39726-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="39726-130">NOTES</span></span>

## <span data-ttu-id="39726-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39726-131">RELATED LINKS</span></span>

[<span data-ttu-id="39726-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39726-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="39726-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39726-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="39726-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39726-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="39726-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39726-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="39726-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39726-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="39726-137">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39726-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="39726-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39726-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
