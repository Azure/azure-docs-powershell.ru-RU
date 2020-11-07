---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732690"
---
# <span data-ttu-id="1085e-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="1085e-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="1085e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1085e-102">SYNOPSIS</span></span>
<span data-ttu-id="1085e-103">Установка профиля шлюза управления сервером.</span><span class="sxs-lookup"><span data-stu-id="1085e-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1085e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1085e-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1085e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1085e-105">DESCRIPTION</span></span>
<span data-ttu-id="1085e-106">Командлет **Install-AzureRmServerManagementGatewayProfile** устанавливает профиль шлюза службы управления сервером Azure Server в нужное расположение.</span><span class="sxs-lookup"><span data-stu-id="1085e-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="1085e-107">Файл, который устанавливает этот командлет, называется profile.js.</span><span class="sxs-lookup"><span data-stu-id="1085e-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="1085e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1085e-108">EXAMPLES</span></span>

## <span data-ttu-id="1085e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1085e-109">PARAMETERS</span></span>

### <span data-ttu-id="1085e-110">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1085e-110">-InputFile</span></span>
<span data-ttu-id="1085e-111">Указывает имя локального файла, который содержит профиль шлюза для установки.</span><span class="sxs-lookup"><span data-stu-id="1085e-111">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="1085e-112">Файл, который устанавливает этот командлет, должен быть ранее сохранен с помощью командлета Save-AzureRmServerManagementGatewayProfile.</span><span class="sxs-lookup"><span data-stu-id="1085e-112">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1085e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1085e-113">-DefaultProfile</span></span>
<span data-ttu-id="1085e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1085e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1085e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1085e-115">CommonParameters</span></span>
<span data-ttu-id="1085e-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1085e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1085e-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1085e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1085e-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1085e-118">INPUTS</span></span>

### <span data-ttu-id="1085e-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="1085e-119">FileInfo</span></span>
<span data-ttu-id="1085e-120">Параметр "InputFile" принимает значение типа FileInfo из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1085e-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="1085e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1085e-121">OUTPUTS</span></span>

## <span data-ttu-id="1085e-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="1085e-122">NOTES</span></span>

## <span data-ttu-id="1085e-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1085e-123">RELATED LINKS</span></span>

[<span data-ttu-id="1085e-124">Сброс — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="1085e-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="1085e-125">Сохранить — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="1085e-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


