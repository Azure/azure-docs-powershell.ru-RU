---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: 37db0181ea135a0cdb00cddc0a18780fe9fe2d7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734222"
---
# <span data-ttu-id="e6247-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e6247-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="e6247-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6247-102">SYNOPSIS</span></span>
<span data-ttu-id="e6247-103">Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="e6247-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6247-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6247-104">SYNTAX</span></span>

### <span data-ttu-id="e6247-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6247-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6247-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e6247-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6247-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e6247-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6247-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6247-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6247-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6247-109">DESCRIPTION</span></span>
<span data-ttu-id="e6247-110">С помощью **Add-AzureRmServiceFabricClientCertificate** добавьте в кластер общего имени и отпечаток поставщика или отпечаток сертификата, чтобы клиент мог использовать его для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e6247-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="e6247-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6247-111">EXAMPLES</span></span>

### <span data-ttu-id="e6247-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6247-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -IsAdmin
```

<span data-ttu-id="e6247-113">Эта команда добавит сертификат с отпечатком "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер, чтобы клиент мог использовать этот сертификат в качестве администратора для связи с кластером.</span><span class="sxs-lookup"><span data-stu-id="e6247-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="e6247-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e6247-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="e6247-115">Эта команда добавит сертификат клиента только для чтения с общим именем "Contoso.com", а отпечаток поставщика — "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер.</span><span class="sxs-lookup"><span data-stu-id="e6247-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="e6247-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6247-116">PARAMETERS</span></span>

### <span data-ttu-id="e6247-117">-Администратор</span><span class="sxs-lookup"><span data-stu-id="e6247-117">-Admin</span></span>
<span data-ttu-id="e6247-118">Тип проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="e6247-118">Client authentication type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6247-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="e6247-120">Укажите отпечаток сертификата клиента, у которого есть разрешение администратора.</span><span class="sxs-lookup"><span data-stu-id="e6247-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="e6247-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="e6247-122">Укажите общее имя клиента, отпечаток поставщика и тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e6247-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="e6247-123">-CommonName</span></span>
<span data-ttu-id="e6247-124">Укажите общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="e6247-124">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-125">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6247-125">-IssuerThumbprint</span></span>
<span data-ttu-id="e6247-126">Укажите отпечаток поставщика сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="e6247-126">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6247-127">-Name</span></span>
<span data-ttu-id="e6247-128">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="e6247-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-129">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6247-129">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="e6247-130">Укажите отпечаток сертификата клиента с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e6247-130">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6247-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6247-132">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6247-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e6247-133">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="e6247-133">-Thumbprint</span></span>
<span data-ttu-id="e6247-134">Укажите отпечаток сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="e6247-134">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6247-135">-Confirm</span></span>
<span data-ttu-id="e6247-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6247-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6247-137">-WhatIf</span></span>
<span data-ttu-id="e6247-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6247-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6247-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6247-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6247-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6247-140">-DefaultProfile</span></span>
<span data-ttu-id="e6247-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6247-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6247-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6247-142">CommonParameters</span></span>
<span data-ttu-id="e6247-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6247-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6247-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6247-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6247-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6247-145">INPUTS</span></span>

### <span data-ttu-id="e6247-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6247-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="e6247-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e6247-147">System.String</span></span>

<span data-ttu-id="e6247-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6247-148">System.Boolean</span></span>

## <span data-ttu-id="e6247-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6247-149">OUTPUTS</span></span>

### <span data-ttu-id="e6247-150">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="e6247-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="e6247-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6247-151">NOTES</span></span>

## <span data-ttu-id="e6247-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6247-152">RELATED LINKS</span></span>

[<span data-ttu-id="e6247-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e6247-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
