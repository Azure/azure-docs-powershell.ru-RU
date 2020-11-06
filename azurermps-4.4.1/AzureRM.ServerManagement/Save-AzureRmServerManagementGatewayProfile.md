---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: af7184b3e43d2016ff4acc9e7634f831945a8fdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567509"
---
# <span data-ttu-id="de6f0-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="de6f0-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="de6f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="de6f0-103">Загружает профиль для шлюза управления сервером и сохраняет его в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="de6f0-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de6f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de6f0-104">SYNTAX</span></span>

### <span data-ttu-id="de6f0-105">ByName</span><span class="sxs-lookup"><span data-stu-id="de6f0-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f0-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="de6f0-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de6f0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de6f0-107">DESCRIPTION</span></span>
<span data-ttu-id="de6f0-108">Командлет **Save-AzureRmServerManagementGatewayProfile** загружает профиль для шлюза службы Azure Server Management и сохраняет его в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="de6f0-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="de6f0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de6f0-109">EXAMPLES</span></span>

## <span data-ttu-id="de6f0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de6f0-110">PARAMETERS</span></span>

### <span data-ttu-id="de6f0-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="de6f0-111">-Gateway</span></span>
<span data-ttu-id="de6f0-112">Указывает шлюз, для которого этот командлет получает профиль.</span><span class="sxs-lookup"><span data-stu-id="de6f0-112">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="de6f0-113">Может использоваться вместо указания ResourceGroupName и GatewayName</span><span class="sxs-lookup"><span data-stu-id="de6f0-113">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de6f0-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="de6f0-114">-GatewayName</span></span>
<span data-ttu-id="de6f0-115">Указывает имя шлюза, для которого этот командлет получает профиль.</span><span class="sxs-lookup"><span data-stu-id="de6f0-115">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de6f0-116">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="de6f0-116">-OutputFile</span></span>
<span data-ttu-id="de6f0-117">Задает локальный файл, в котором нужно сохранить данные профиля.</span><span class="sxs-lookup"><span data-stu-id="de6f0-117">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6f0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6f0-118">-ResourceGroupName</span></span>
<span data-ttu-id="de6f0-119">Указывает имя группы ресурсов, к которой принадлежит шлюз.</span><span class="sxs-lookup"><span data-stu-id="de6f0-119">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de6f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6f0-120">-DefaultProfile</span></span>
<span data-ttu-id="de6f0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de6f0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de6f0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6f0-122">CommonParameters</span></span>
<span data-ttu-id="de6f0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de6f0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6f0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de6f0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6f0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de6f0-125">INPUTS</span></span>

### <span data-ttu-id="de6f0-126">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="de6f0-126">Gateway</span></span>
<span data-ttu-id="de6f0-127">Параметр Gateway принимает от конвейера значение типа Gateway.</span><span class="sxs-lookup"><span data-stu-id="de6f0-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="de6f0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de6f0-128">OUTPUTS</span></span>

### <span data-ttu-id="de6f0-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="de6f0-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="de6f0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="de6f0-130">NOTES</span></span>

## <span data-ttu-id="de6f0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de6f0-131">RELATED LINKS</span></span>

[<span data-ttu-id="de6f0-132">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="de6f0-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="de6f0-133">Сброс — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="de6f0-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


