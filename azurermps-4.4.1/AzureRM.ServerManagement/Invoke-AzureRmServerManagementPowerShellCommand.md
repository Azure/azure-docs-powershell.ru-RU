---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: 5acd510118f2be26ba09f3e0fefbc9b0c80aae02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565147"
---
# <span data-ttu-id="c7a35-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="c7a35-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="c7a35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7a35-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a35-103">Выполняет блок сценария Windows PowerShell на узле.</span><span class="sxs-lookup"><span data-stu-id="c7a35-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7a35-104">SYNTAX</span></span>

### <span data-ttu-id="c7a35-105">ByName</span><span class="sxs-lookup"><span data-stu-id="c7a35-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a35-106">BySession</span><span class="sxs-lookup"><span data-stu-id="c7a35-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a35-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7a35-107">DESCRIPTION</span></span>
<span data-ttu-id="c7a35-108">Командлет **Invoke-AzureRmServerManagementPowerShellCommand** выполняет блок сценария Windows PowerShell на узле, управляемом шлюзом управления сервером Azure Server.</span><span class="sxs-lookup"><span data-stu-id="c7a35-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="c7a35-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7a35-109">EXAMPLES</span></span>

## <span data-ttu-id="c7a35-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7a35-110">PARAMETERS</span></span>

### <span data-ttu-id="c7a35-111">-Command</span><span class="sxs-lookup"><span data-stu-id="c7a35-111">-Command</span></span>
<span data-ttu-id="c7a35-112">Задает блок сценария для выполнения на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="c7a35-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: System.Management.Automation.ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a35-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="c7a35-113">-NodeName</span></span>
<span data-ttu-id="c7a35-114">Указывает имя узла, для которого нужно запустить блок сценария.</span><span class="sxs-lookup"><span data-stu-id="c7a35-114">Specifies the name of the node to run the script block on.</span></span>

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

### <span data-ttu-id="c7a35-115">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="c7a35-115">-PowerShellSessionName</span></span>
<span data-ttu-id="c7a35-116">Указывает имя пространства выполнения Windows PowerShell на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="c7a35-116">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a35-117">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="c7a35-117">-RawOutput</span></span>
<span data-ttu-id="c7a35-118">Указывает на то, что командлет возвращает полный объект, содержащий выходные данные узла.</span><span class="sxs-lookup"><span data-stu-id="c7a35-118">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a35-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a35-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7a35-120">Указывает имя группы ресурсов, к которой принадлежит узел.</span><span class="sxs-lookup"><span data-stu-id="c7a35-120">Specifies the name of the resource group that the node belongs to.</span></span>

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

### <span data-ttu-id="c7a35-121">-Session</span><span class="sxs-lookup"><span data-stu-id="c7a35-121">-Session</span></span>
<span data-ttu-id="c7a35-122">Указывает объект **сеанса** , используемый этим командлетом для подключения к целевому узлу.</span><span class="sxs-lookup"><span data-stu-id="c7a35-122">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="c7a35-123">Этот параметр может быть указан вместо параметров *ResourceGroupName* , *nodeName* , *SessionName* и *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="c7a35-123">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a35-124">-SessionName</span><span class="sxs-lookup"><span data-stu-id="c7a35-124">-SessionName</span></span>
<span data-ttu-id="c7a35-125">Указывает имя сеанса для управления узлом.</span><span class="sxs-lookup"><span data-stu-id="c7a35-125">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a35-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a35-126">-DefaultProfile</span></span>
<span data-ttu-id="c7a35-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a35-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a35-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a35-128">CommonParameters</span></span>
<span data-ttu-id="c7a35-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7a35-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a35-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a35-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a35-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7a35-131">INPUTS</span></span>

### <span data-ttu-id="c7a35-132">Сесси</span><span class="sxs-lookup"><span data-stu-id="c7a35-132">Session</span></span>
<span data-ttu-id="c7a35-133">Параметр Session принимает значение типа Session из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c7a35-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="c7a35-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7a35-134">OUTPUTS</span></span>

### <span data-ttu-id="c7a35-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="c7a35-135">System.Object</span></span>

## <span data-ttu-id="c7a35-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7a35-136">NOTES</span></span>

## <span data-ttu-id="c7a35-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7a35-137">RELATED LINKS</span></span>

[<span data-ttu-id="c7a35-138">Командлеты управления сервером Azure</span><span class="sxs-lookup"><span data-stu-id="c7a35-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


