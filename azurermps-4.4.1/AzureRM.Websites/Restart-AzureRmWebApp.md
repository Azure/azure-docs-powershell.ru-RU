---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: eb75a4fa0ebeb121cd39e591b8cb8d46909deb42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557683"
---
# <span data-ttu-id="3728b-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="3728b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3728b-102">SYNOPSIS</span></span>
<span data-ttu-id="3728b-103">Перезапускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="3728b-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3728b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3728b-104">SYNTAX</span></span>

### <span data-ttu-id="3728b-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="3728b-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3728b-106">S2</span><span class="sxs-lookup"><span data-stu-id="3728b-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3728b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3728b-107">DESCRIPTION</span></span>
<span data-ttu-id="3728b-108">Командлет **restart-AzureRmWebApp** останавливается, а затем запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="3728b-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="3728b-109">Если веб-приложение находится в остановленном состоянии, используйте командлет Start-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="3728b-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="3728b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3728b-110">EXAMPLES</span></span>

### <span data-ttu-id="3728b-111">Пример 1: перезагрузка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3728b-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3728b-112">Эта команда останавливает веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов Default-Web-WestUS, а затем перезапускает ее.</span><span class="sxs-lookup"><span data-stu-id="3728b-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="3728b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3728b-113">PARAMETERS</span></span>

### <span data-ttu-id="3728b-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3728b-114">-Name</span></span>
<span data-ttu-id="3728b-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-115">WebApp Name</span></span>

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

### <span data-ttu-id="3728b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3728b-116">-ResourceGroupName</span></span>
<span data-ttu-id="3728b-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3728b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="3728b-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-118">-WebApp</span></span>
<span data-ttu-id="3728b-119">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3728b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3728b-120">-DefaultProfile</span></span>
<span data-ttu-id="3728b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3728b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3728b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3728b-122">CommonParameters</span></span>
<span data-ttu-id="3728b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3728b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3728b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3728b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3728b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3728b-125">INPUTS</span></span>

### <span data-ttu-id="3728b-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="3728b-126">Site</span></span>
<span data-ttu-id="3728b-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3728b-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3728b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3728b-128">OUTPUTS</span></span>

## <span data-ttu-id="3728b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="3728b-129">NOTES</span></span>

## <span data-ttu-id="3728b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3728b-130">RELATED LINKS</span></span>

[<span data-ttu-id="3728b-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="3728b-132">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="3728b-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3728b-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3728b-135">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3728b-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


