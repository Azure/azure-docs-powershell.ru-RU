---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734220"
---
# <span data-ttu-id="1b576-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1b576-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="1b576-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b576-102">SYNOPSIS</span></span>
<span data-ttu-id="1b576-103">Возвращает сведения о серверах восстановления сайта, зарегистрированных в текущем хранилище.</span><span class="sxs-lookup"><span data-stu-id="1b576-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b576-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b576-104">SYNTAX</span></span>

### <span data-ttu-id="1b576-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b576-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b576-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1b576-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b576-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="1b576-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b576-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b576-108">DESCRIPTION</span></span>
<span data-ttu-id="1b576-109">Командлет **Get-AzureRmSiteRecoveryServer** получает сведения о серверах Azure Site Recovery, зарегистрированных в текущем хранилище сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b576-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="1b576-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b576-110">EXAMPLES</span></span>

## <span data-ttu-id="1b576-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b576-111">PARAMETERS</span></span>

### <span data-ttu-id="1b576-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1b576-112">-FriendlyName</span></span>
<span data-ttu-id="1b576-113">Указывает понятное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1b576-113">Specifies the friendly name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b576-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b576-114">-Name</span></span>
<span data-ttu-id="1b576-115">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1b576-115">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b576-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b576-116">-DefaultProfile</span></span>
<span data-ttu-id="1b576-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b576-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b576-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b576-118">CommonParameters</span></span>
<span data-ttu-id="1b576-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b576-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b576-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b576-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b576-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b576-121">INPUTS</span></span>

## <span data-ttu-id="1b576-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b576-122">OUTPUTS</span></span>

### <span data-ttu-id="1b576-123">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="1b576-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="1b576-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b576-124">NOTES</span></span>

## <span data-ttu-id="1b576-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b576-125">RELATED LINKS</span></span>

[<span data-ttu-id="1b576-126">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1b576-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
