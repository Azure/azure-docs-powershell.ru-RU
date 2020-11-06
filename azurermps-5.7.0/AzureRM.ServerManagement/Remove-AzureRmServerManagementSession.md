---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: b2ebde9e6cf0e94e43d41cd75ee7ee09674fc3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567400"
---
# <span data-ttu-id="c772b-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="c772b-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="c772b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c772b-102">SYNOPSIS</span></span>
<span data-ttu-id="c772b-103">Удаление сеанса управления сервером.</span><span class="sxs-lookup"><span data-stu-id="c772b-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c772b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c772b-104">SYNTAX</span></span>

### <span data-ttu-id="c772b-105">ByName</span><span class="sxs-lookup"><span data-stu-id="c772b-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c772b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c772b-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c772b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c772b-107">DESCRIPTION</span></span>
<span data-ttu-id="c772b-108">Командлет **Remove-AzureRmServerManagementSession** удаляет сеанс управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="c772b-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="c772b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c772b-109">EXAMPLES</span></span>

## <span data-ttu-id="c772b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c772b-110">PARAMETERS</span></span>

### <span data-ttu-id="c772b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c772b-111">-DefaultProfile</span></span>
<span data-ttu-id="c772b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c772b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c772b-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="c772b-113">-NodeName</span></span>
<span data-ttu-id="c772b-114">Указывает имя узла, на котором этот командлет удаляет сеанс.</span><span class="sxs-lookup"><span data-stu-id="c772b-114">Specifies the name of the node on which this cmdlet removes the session.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c772b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c772b-115">-ResourceGroupName</span></span>
<span data-ttu-id="c772b-116">Указывает имя группы ресурсов, к которой относится сеанс.</span><span class="sxs-lookup"><span data-stu-id="c772b-116">Specifies the name of the resource group that the session belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c772b-117">-Session</span><span class="sxs-lookup"><span data-stu-id="c772b-117">-Session</span></span>
<span data-ttu-id="c772b-118">Указывает сеанс, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c772b-118">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="c772b-119">Этот параметр можно использовать вместо параметров *ResourceGroupName* , *nodeName* и *SessionName* .</span><span class="sxs-lookup"><span data-stu-id="c772b-119">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c772b-120">-SessionName</span><span class="sxs-lookup"><span data-stu-id="c772b-120">-SessionName</span></span>
<span data-ttu-id="c772b-121">Указывает имя сеанса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c772b-121">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c772b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c772b-122">CommonParameters</span></span>
<span data-ttu-id="c772b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c772b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c772b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c772b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c772b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c772b-125">INPUTS</span></span>

### <span data-ttu-id="c772b-126">Сесси</span><span class="sxs-lookup"><span data-stu-id="c772b-126">Session</span></span>
<span data-ttu-id="c772b-127">Параметр Session принимает значение типа Session из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c772b-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="c772b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c772b-128">OUTPUTS</span></span>

## <span data-ttu-id="c772b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c772b-129">NOTES</span></span>

## <span data-ttu-id="c772b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c772b-130">RELATED LINKS</span></span>

[<span data-ttu-id="c772b-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="c772b-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="c772b-132">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="c772b-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


