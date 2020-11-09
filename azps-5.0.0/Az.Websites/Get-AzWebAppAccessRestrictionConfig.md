---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245736"
---
# <span data-ttu-id="a3ead-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a3ead-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="a3ead-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3ead-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ead-103">Получает доступ к конфигурации restiction для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ead-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="a3ead-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3ead-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3ead-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3ead-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ead-106">Командлет **Get-AzWebAppAccessRestrictionConfig** получает конфигурацию ограничения доступа к веб-приложению Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ead-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="a3ead-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3ead-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ead-108">Пример 1: получение конфигурации ограничения доступа для веб-приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a3ead-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="a3ead-109">Эта команда получает конфигурацию ограничения доступа для веб-приложения с именем ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a3ead-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a3ead-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3ead-110">PARAMETERS</span></span>

### <span data-ttu-id="a3ead-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ead-111">-DefaultProfile</span></span>
<span data-ttu-id="a3ead-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ead-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3ead-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3ead-113">-Name</span></span>
<span data-ttu-id="a3ead-114">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="a3ead-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ead-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ead-115">-ResourceGroupName</span></span>
<span data-ttu-id="a3ead-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a3ead-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ead-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a3ead-117">-SlotName</span></span>
<span data-ttu-id="a3ead-118">Имя слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="a3ead-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="a3ead-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ead-119">CommonParameters</span></span>
<span data-ttu-id="a3ead-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3ead-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ead-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3ead-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ead-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3ead-122">INPUTS</span></span>

### <span data-ttu-id="a3ead-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a3ead-123">System.String</span></span>

## <span data-ttu-id="a3ead-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3ead-124">OUTPUTS</span></span>

### <span data-ttu-id="a3ead-125">Microsoft. Azure. Commands. Apps. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a3ead-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="a3ead-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3ead-126">NOTES</span></span>

## <span data-ttu-id="a3ead-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3ead-127">RELATED LINKS</span></span>

[<span data-ttu-id="a3ead-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a3ead-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a3ead-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a3ead-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="a3ead-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a3ead-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)